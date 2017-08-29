# Método Blockchain.GetHeight()

Devuelve el tamaño del bloque actual de la blockchain. Tamaño del bloque = índice del bloque = nº de bloques - 1.

Namespace: [FRS.SmartContract.Framework.Services.FRS](../../FRS.md)

Assembly: FRS.SmartContract.Framework

## Sintaxis

```c#
public static extern uint GetHeight ()
```

Valor de retorno: Tamaño del bloque, del tipo unsigned integer.

## Ejemplo

```c#
public class Contract1: FunctionCode
{
     public static void Main ()
     {
         Uint height = Blockchain.GetHeight ();
     }
}
```



[Volver arriba](../Blockchain.md)
