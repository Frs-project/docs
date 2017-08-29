# Storage.Delete method (StorageContext, string)

Delete the operation, in the persistent storage area through the key to delete the corresponding value.

Namespace: [FRS.SmartContract.Framework.Services.FRS](../../FRS.md)

Assembly: FRS.SmartContract.Framework

## Sintaxis

```c#
public extern void Delete (FRS.SmartContract.Framework.Services.FRS.StorageContext context, byte[] key)
```

## Parámetros

Context: Contexto de almacenamiento [StorageContext](../StorageContex.md) type.

Key: clave, tipo string

Valor devuelto: void.

## Ejemplo

```c#
public class Contract1: FunctionCode
{
     public static void Main ()
     {
         Storage.Delete (Storage.CurrentContext, "Key");
     }
}
```



[Volver arriba](../Storage.md)
