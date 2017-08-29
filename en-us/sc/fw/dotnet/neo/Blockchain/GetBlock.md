# Blockchain.GetBlock Method (byte[])

Returns a block from the blockchain given a block hash.

Namespace: [FRS.SmartContract.Framework.Services.FRS](../../FRS.md)

Assembly: FRS.SmartContract.Framework

## Syntax

```c#
public static extern FRS.SmartContract.Framework.Services.FRS.Block GetBlock(byte[] hash)
```

Parameters: Block Hash as a byte array of length 32.

Return Value: [Block](../Block.md).

## Example

```c#
public class Contract1: FunctionCode
{
     public static void Main()
     {
         byte[] block = new byte[] {206, 240, 165, 25, 76, 228, 58, 100, 117, 184, 213, 171, 61, 96, 34, 234, 129, 116, 60, 71, 11, 231, 143, 195, 123, 5, 190, 250, 182, 14, 152};
         Block bl = Blockchain.GetBlock(block);
     }
}
```



[Back](../Blockchain.md)
