# Block.GetTransactions Method ()

Returns all the transactions in the current block.

Namespace: [FRS.SmartContract.Framework.Services.FRS](../../FRS.md)

Assembly: FRS.SmartContract.Framework

## Syntax

```c#
public extern FRS.SmartContract.Framework.Services.FRS.Transaction[] GetTransactions()
```

Return Value: Transaction array as Transaction[].

## Example

```c#
public class Contract1: FunctionCode
{
     public static void Main()
     {
         Block block = Blockchain.GetBlock(997027);
         Transaction[] txs = block.GetTransactions();
     }
}
```



[Back](../Block.md)
