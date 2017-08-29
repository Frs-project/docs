# Método Block.GetTransaction(int)

Devuelve la transacción especificada por el índice del actual bloque.

Namespace: [FRS.SmartContract.Framework.Services.FRS](../../FRS.md)

Assembly: FRS.SmartContract.Framework

## Sintaxis

```c#
public extern FRS.SmartContract.Framework.Services.FRS.Transaction GetTransaction (int index)
```

Parámetros: El índice de la transacción en el bloque, un entero

Valor de retorno: Transacción del tipo [Transaccion](../Transaction.md).

## Ejemplo

```c#
public class Contract1: FunctionCode
{
     public static void Main ()
     {
         Block block = Blockchain.GetBlock (997027);
         Transaction tx = block.GetTransaction (0);
     }
}
```



[Volver arriba](../Block.md)
