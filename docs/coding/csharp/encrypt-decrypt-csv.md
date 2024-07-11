---
sidebar_position: 3
---

# Encrypt & Decrypt CSV - Still In Progress...

To encrypt and decrypt a CSV file in C#, you can use a combination of cryptographic functions and file I/O operations.

Here is the example `System.Security.Cryptography` for encryption and decryption:

### Encryption:

```javascript
using (Aes aesAlg = Aes.Create())
{
    string inputFilePath = "Your Input File Path";
    string encryptedFilePath = "Your Encrypted File Path";
    aesAlg.Key = Encoding.UTF8.GetBytes("Your EncryptKey"); //the EncryptKey is a 32 bytes and can put from webconfig
    aesAlg.GenerateIV();

    byte[] encryptedBytes;

    using (MemoryStream memoryStream = new MemoryStream())
    {
        using (CryptoStream cs = new CryptoStream(memoryStream, aesAlg.CreateEncryptor(), CryptoStreamMode.Write))
        using (StreamWriter sw = new StreamWriter(cs))
        {
            sw.Write(inputFilePath);
        }

        encryptedBytes = memoryStream.ToArray();
    }

    File.WriteAllBytes(encryptedFilePath, aesAlg.IV.Concat(encryptedBytes).ToArray());

}
```

### Decryption:

```javascript
byte[] encryptedBytesWithIV = File.ReadAllBytes("Your Target File Path");
using (Aes aesAlg = Aes.Create())
{
    aesAlg.Key = Encoding.UTF8.GetBytes("Your Key"); //the EncryptKey is a 32 bytes and can put from webconfig

    byte[] iv = new byte[aesAlg.IV.Length];
    Array.Copy(encryptedBytesWithIV, iv, iv.Length);
    

    using (MemoryStream memoryStream = new MemoryStream(encryptedBytesWithIV, iv.Length, encryptedBytesWithIV.Length - iv.Length))
    using (CryptoStream cs = new CryptoStream(memoryStream, aesAlg.CreateDecryptor(aesAlg.Key, iv), CryptoStreamMode.Read))
    using (StreamReader sr = new StreamReader(cs))
    {
        return sr.ReadToEnd();
    }
}
```
