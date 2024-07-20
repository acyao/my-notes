---
sidebar_position: 6
---

# Steps to convert AAB to APK

When we generate the aab and need to test and debug the application but aab unable to install directly in phone. So we have to convert aab to apk to do the testing.

1. download bundletool https://developer.android.com/tools/bundletool

2. open the cmd

3. run this command, will generate the apks. ks is keystore* ks-key-alias is alias name.

```
java -jar "D:\Users\XXX\Documents\aab convert apk\bundletool-all-1.8.1.jar" build-apks --bundle="D:\Users\XXXX\Documents\aab convert apk\XXXXXX.aab" --output="D:\Users\XXXX\Documents\aab convert apk\XXXXXX.apks" --ks="D:\Users\XXX\Documents\aab convert apk\XXXXXX.keystore" --ks-key-alias=itapps --mode=universal
```

4. after generated the apks and change the .apks to .zip

5. extract the zip to get the apk