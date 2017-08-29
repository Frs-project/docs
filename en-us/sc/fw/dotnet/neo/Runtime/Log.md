# Runtime.Log Method (string)

Sends a log message to the client executing the smart contract. This method can trigger an event on the client but will require the client to be compatible.

Namespace: [FRS.SmartContract.Framework.Services.FRS](../../FRS.md)

Assembly: FRS.SmartContract.Framework

## Syntax

```c#
public static extern void Log(string message)
```

Parameters: 

message: Log as a string.

## Example

```c#
public class Contract1 : FunctionCode
{
    public static void Main(bool debug)
    {
        if(debug)
        {
            Runtime.Log("Execution successful");
        }
    }
}
```



[Back](../Runtime.md)