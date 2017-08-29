# Método Transaction.GetOutputs()

Retorna todas las transacciones para la transacción actual.

Namespace: [FRS.SmartContract.Framework.Services.FRS](../../FRS.md)

Assembly: FRS.SmartContract.Framework

## Sintaxis

```c#
public extern FRS.SmartContract.Framework.Services.FRS.TransactionOutput[] GetOutputs ()
```

Valor de retorno: Array del tipo [TransactionOutput](../TransactionOutput.md) con todas las transacciones para la transacción actual.

## Ejemplo

```c#
public class Contract1: FunctionCode
{
     public static void Main ()
     {
         byte[] transaction = new byte[] {88, 114, 160, 206, 130, 137, 41, 94, 119, 120, 242, 71, 232, 244, 3, 20, 165, 69, 182, 106, 185, 119, 239, 183, 65, 174, 220, 157, 251, 28, 215};
         Transaction tx = Blockchain.GetTransaction (transaction);
         TransactionOutput[] = tx.GetOutputs ();
     }
}
```



[Volver arriba](../Transaction.md)
