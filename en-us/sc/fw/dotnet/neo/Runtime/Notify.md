# Runtime.Notify Method (params object[])

Similar to Runtime.Log, this notifies the client by the executing smart contract. This method can trigger an event on the client but will require the client to be compatible.

Namespace: [FRS.SmartContract.Framework.Services.FRS](../../FRS.md)

Assembly: FRS.SmartContract.Framework

## Syntax

```c#
public static extern void Notify(params object[] state)
```

Parameters: 

state: The notification message, can be of any length and any type.

## Example

```c#
public class Contract1 : FunctionCode
{
    public static void Main()
    {
        Runtime.Notify("Hello", "World", Blockchain.GetHeight());
    }
}
```



[Back](../Runtime.md)