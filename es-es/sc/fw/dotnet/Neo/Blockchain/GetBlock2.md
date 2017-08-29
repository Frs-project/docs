# Método Blockchain.GetBlock(uint)

Busca un bloque por el tamaño de este.

Namespace: [FRS.SmartContract.Framework.Services.FRS](../../FRS.md)

Assembly: FRS.SmartContract.Framework

## Sintaxis

```c#
public static extern FRS.SmartContract.Framework.Services.FRS.Block GetBlock (uint height)
```

Parámetros: Tamaño del bloque (índice del bloque), de tipo unsigned integer.

Valor de retorno: [Block](../Block.md).

## Ejemplo

```c#
public class Contract1: FunctionCode
{
     public static void Main ()
     {
         Block bl = Blockchain.GetBlock (997027);
     }
}
```





[Volver arriba](../Blockchain.md)
