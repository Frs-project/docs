# Blockchain.GetBlock Method (uint)

Returns a block from the blockchain given a block height.

Namespace: [FRS.SmartContract.Framework.Services.FRS](../../FRS.md)

Assembly: FRS.SmartContract.Framework

## Syntax

```c#
public static extern FRS.SmartContract.Framework.Services.FRS.Block GetBlock(uint height)
```

Parameters: Block height (block index) as an unsigned integer.

Return Value: [Block](../Block.md).

## Example

```c#
public class Contract1: FunctionCode
{
     public static void Main()
     {
         Block bl = Blockchain.GetBlock(997027);
     }
}
```



[Back](../Blockchain.md)
