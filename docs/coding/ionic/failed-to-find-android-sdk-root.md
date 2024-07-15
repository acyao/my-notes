---
sidebar_position: 3
---

# Failed to find 'ANDROID_SDK_ROOT' environment variable

## Issue Faced:

![failed to find android sdk root](/img/failed-to-find-android-sdk-root.png)

- Failed to find 'ANDROID_SDK_ROOT' environment variable. Try setting it manually.
- Failed to find 'android' command in your 'PATH'. Try update your 'PATH' to include path to valid SDK directory.

## Solution:

1. open the Edit Environment Variables.

2. add ANDROID_HOME in the environment variable.

    `C:\Users\XXXXXXX\AppData\Local\Android\Sdk`

3. edit PATH in the environment variable.

    `C:\Users\XXXXXXX\AppData\Local\Android\Sdk\platform-tools`