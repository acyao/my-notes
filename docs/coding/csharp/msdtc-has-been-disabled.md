# Steps to enable MSDTC

## Issue Faced:

System.Transactions.TransactionManagerCommunicationException: Network access for Distributed Transaction Manager (MSDTC) has been disabled. Please enable DTC for network access in the security configuration for MSDTC using the Component Services Administrative tool

## Solution:

1. Open **Run** type `dcomcnfg`. It will open **Component Service** window.

2. Expand the **Component Service**, expand the **My Computer**, expand the **Distributed Transaction Coordinator**

    ![Component Service](/img/component-service.png)

3. You will see the **Local DTC**, Right click on it, and click **Properties**. It will open the **Local DTC Properties**

    ![Local DTC Properties](/img/local-DTC-properties.png)

4. Click **Security** tab

5. Tick the **Network DTC Access** checkbox.

6. Tick the **Allow Inbound** and **Allow Outbound** under the Transaction Manager Communication.

    ![Security Local DTC](/img/security-local-DTC.png)

7. Click **Apply** and **OK**.