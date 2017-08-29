# Método Block.GetTransactionCount()

Devuelve el número de transacciones en el bloque actual.

Namespace: [FRS.SmartContract.Framework.Services.FRS](../../FRS.md)

Assembly: FRS.SmartContract.Framework

## Sintaxis

```c#
public extern int GetTransactionCount ()
```

Valor de retorno: número de transacciones, integer.

## Ejemplo

```c#
public class Contract1: FunctionCode
{
     public static void Main ()
     {
         Block block = Blockchain.GetBlock (997027);
         Int txCount = block.GetTransactionCount ();
     }
}
```



[Volver arriba](../Block.md)
