---
sidebar_position: 2
---
# Steps to deploy AAB to Google Play

1. First need to build

```
ionic cordova build android
```

2. go to plafrom/android path

```
cd platforms/android
```

3. run the gradlew bundle

```
.\gradlew bundle
```

4. after that it will generate release aab, the aab file locate at the outputs/bundle/release folder

`platforms/android/app/build/outputs/bundle/release folder`

5. Sign the unsigned apk

```
jarsigner -verbose -sigalg SHA1withRSA -digestalg SHA1 -keystore my-release-key.keystore app-release-unsigned.apk alias_name
```

6.  Zipalign is to optimize the apk. Copy signed apk to Android/Sdk/build-tools/Version.

```
zipalign -v 4 HelloWorld-signed.apk HelloWorld.apk
```