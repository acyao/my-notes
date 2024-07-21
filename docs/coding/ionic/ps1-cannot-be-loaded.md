# ionic.ps1 cannot be loaded because running scripts is disabled on this system

## Issue Faced:

![ps1 cannot be loaded](/img/ps1-cannot-be-loaded.png)

## Solution:

![](/img/power-shell-set-executionpolicy.png)

Open PowerShell as administrator and type `Set-ExecutionPolicy Unrestricted`