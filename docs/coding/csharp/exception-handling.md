---
sidebar_position: 1
---

# Exception Handling

In C#, exception handling is done using `try`, `catch`, `finally`, and `throw` statements. 

- `try`: code that might throw an exception.
- `catch`: catches and handles exception thrown by code in the `try` block.
- `finally`: optinal. executed after the `try` block. It is used to cleanup code.
- `throw`: used to throw an exception. 



```c#
try
{

}
catch (Exception ex)
{
    throw new Exception("Error: " + ex.Message);
}
finally
{
    //cleanup
}
```