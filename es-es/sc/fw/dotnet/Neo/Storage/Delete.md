# Método Storage.Delete (StorageContext, byte[])

Operación de borrado en el área del almacenamiento persistente a través de una clave para borrar el correspondiente valor.

Namespace: [FRS.SmartContract.Framework.Services.FRS](../../FRS.md)

Assembly: FRS.SmartContract.Framework

## Sintaxis

```c#
public extern void Delete (FRS.SmartContract.Framework.Services.FRS.StorageContext context, byte[] key)
```

## Parámetros:

Context: Contexto de almacenamiento, tipo [StorageContext](../StorageContex.md)

Key: clave, tipo array de byte.

Valor devuelto: void.

## Ejemplo

```c#
public class Contract1: FunctionCode
{
     public static void Main ()
     {
         Storage.Delete (Storage.CurrentContext, new byte[] {0});
     }
}
```



[Volver arriba](../Storage.md)
