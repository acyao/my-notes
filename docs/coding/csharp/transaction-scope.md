---
sidebar_position: 2
---

# Transaction Scope

Manage a block of code as single transaction.

#### Example

```csharp
//Begin transaction scope
using (TransactionScope scope = new TransactionScope())
{
    //Do something...

    //Complete the transaction
    scope.Complete();
}
```

We can set a timeout for `TransactionScope`. If the transaction is not completed within the time, it will be rolled back automatically.

#### Example with timeout

```csharp
// Begin transaction scope with the specified timeout
using (TransactionScope scope = new TransactionScope(TransactionScopeOption.Required, new TimeSpan(0, 10, 0)))
{
    //Do something...

    // Complete the transaction
    scope.Complete();
}
```
