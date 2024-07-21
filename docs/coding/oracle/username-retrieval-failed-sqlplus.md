# Username retrieval failed

## Issue Faced:

When trying to access oracle database with sqlplus on windows server, getting this error.

``ORA-12631: Username retrieval failed on Windows login with sqlplus``

## Solution:

change `SQLNET.AUTHENTICATION_SERVICES= (NTS)` to `SQLNET.AUTHENTICATION_SERVICES = (NONE)` on sqlnet.ora under $$ORACLE_HOME/NETWORK/ADMIN directory.

:::danger Warning
Please backup the sqlnet.ora or command the SQLNET.AUTHENTICATION_SERVICES= (NTS) line.
:::