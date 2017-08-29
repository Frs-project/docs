# Blockchain.GetHeader Method (byte[])

Returns a block header given a block hash.

Namespace: [FRS.SmartContract.Framework.Services.FRS](../../FRS.md)

Assembly: FRS.SmartContract.Framework

## Syntax

```c#
public static extern FRS.SmartContract.Framework.Services.FRS.Header GetHeader(byte[] hash)
```

Parameters: Block Hash as a byte array of length 32.

Return Value: [Header](../Header.md).

## Example

```c#
public class Contract1: FunctionCode
{
     public static void Main()
     {
         byte[] Header = new byte[] {206, 240, 165, 25, 76, 228, 58, 100, 117, 184, 213, 171, 61, 96, 34, 234, 129, 116, 60, 71, 11, 231, 143, 195, 123, 5, 190, 250, 182, 14, 152};
         Header bl = Blockchain.GetHeader(Header);
     }
}
```



[Back](../Blockchain.md)
