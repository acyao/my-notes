---
sidebar_position: 4
---

# Steps to deploy APK to Google Play

1. First need to generate the release apk

```
ionic cordova build android --release
```

2. Open cmd and go the project file path

```
cd Project\FilePath
```

3. Generate keystore using keytool. if keystore already generated then skip this step. 

```
keytool -genkey -v -keystore my-release-key.keystore -alias alias_name -keyalg RSA -keysize 2048 -validity 10000
```

:::danger Warning:
Save and keep keystore in safe place.
:::

4. Sign the unsigned apk

```
jarsigner -verbose -sigalg SHA1withRSA -digestalg SHA1 -keystore my-release-key.keystore app-release-unsigned.apk alias_name
```

5. Zipalign is to optimize the apk. Copy signed apk to Android/Sdk/build-tools/Version

```
zipalign -v 4 HelloWorld-signed.apk HelloWorld.apk
```

6.  To verify the signature of APK. This also can done in the Android/Sdk/build-tools/Version. Remember put copied keystore in the build-tools inside.

```
apksigner sign --ks my-release.keystore --ks-key-alias alias_name applicationName.apk
```

7. Check and verify the status of the APK.

```
apksigner verify -v applicationName.apk
```