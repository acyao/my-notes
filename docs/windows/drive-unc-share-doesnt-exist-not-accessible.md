# The drive or UNC share you selected does not exist or is not accessible. please select another.

## Issue Faced:

![Driver or UNC doest not exist or not accessible](/img/driver-UNC-ShareSelectedDoesntExist.png)

## Solution:

1. Uninstall the visual studio code in the Control Panel\Programs\Programs and Features. If removed or cant found it, skip this step

2. Manual remove the Visual Studio Code registry key in the regedit.

`Computer\HKEY_CURRENT_USER\SOFTWARE\Microsoft\Windows\CurrentVersion\Uninstall\{771FD6B0-FA20-440A-A002-3B3BAC16DC50}_is1`