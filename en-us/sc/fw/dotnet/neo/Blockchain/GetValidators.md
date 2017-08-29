# Blockchain.GetValidators Method ()

Returns the public keys of the validators (consensus nodes).

Namespace: [FRS.SmartContract.Framework.Services.FRS](../../FRS.md)

Assembly: FRS.SmartContract.Framework

## Syntax

```c#
public static extern byte[][] GetValidators()
```

Return Value: A public key array, each element being a byte array of length 33.

## Example

```c#
public class Contract1: FunctionCode
{
     public static void Main()
     {
         byte[][] validators = Blockchain.GetValidators();
     }
}
```



[Back](../Blockchain.md)