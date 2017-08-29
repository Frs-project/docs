# Blockchain.GetHeight Method ()

Returns the current block height of the blockchain. Block height = block index = number of blocks - 1.

Namespace: [FRS.SmartContract.Framework.Services.FRS](../../FRS.md)

Assembly: FRS.SmartContract.Framework

## Syntax

```c#
public static extern uint GetHeight()
```

Return Value: Block height as an unsigned integer.

## Example

```c#
public class Contract1: FunctionCode
{
     public static void Main ()
     {
         Uint height = Blockchain.GetHeight();
     }
}
```



[Back](../Blockchain.md)
