# Método Block.GetTransactions()

Devuelve todas las transacciones en el bloque actual.

Namespace: [FRS.SmartContract.Framework.Services.FRS](../../FRS.md)

Assembly: FRS.SmartContract.Framework

## Sintaxis

```c#
public extern FRS.SmartContract.Framework.Services.FRS.Transaction[] GetTransactions ()
```

Valor de retorno: Array del tipo Transaction, Transaction[].

## Ejemplo

```c#
public class Contract1: FunctionCode
{
     public static void Main ()
     {
         Block block = Blockchain.GetBlock (997027);
         Transaction[] txs = block.GetTransactions ();
     }
}
```



[Volver arriba](../Block.md)
