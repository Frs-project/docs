# Transaction.GetOutputs Method ()

Returns all transaction outputs for the transaction.

Namespace: [FRS.SmartContract.Framework.Services.FRS](../../FRS.md)

Assembly: FRS.SmartContract.Framework

## Syntax

```c#
public extern FRS.SmartContract.Framework.Services.FRS.TransactionOutput[] GetOutputs()
```

Return Value: All transaction outputs for the current transaction as a [TransactionOutput](../TransactionOutput.md) array.

## Example

```c#
public class Contract1: FunctionCode
{
     public static void Main()
     {
         byte[] transaction = new byte[] {88, 114, 160, 206, 130, 137, 41, 94, 119, 120, 242, 71, 232, 244, 3, 20, 165, 69, 182, 106, 185, 119, 239, 183, 65, 174, 220, 157, 251, 28, 215};
         Transaction tx = Blockchain.GetTransaction(transaction);
         TransactionOutput[] = tx.GetOutputs();
     }
}
```



[Back](../Transaction.md)
