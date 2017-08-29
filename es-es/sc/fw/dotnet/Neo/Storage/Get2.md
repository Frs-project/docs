# Storage.Get method (StorageContext, string)

Operación de consulta en el area de almacenamiento persistente a través de una consulta de una clave (string), obteniendo el valor correspondiente.

Namespace: [FRS.SmartContract.Framework.Services.FRS](../../FRS.md)

Assembly: FRS.SmartContract.Framework

## Sintaxis

```c#
public extern void Delete (FRS.SmartContract.Framework.Services.FRS.StorageContext context, string key)
```

## Parámetros:

Context: Context: Contexto de almacenamiento, tipo, [StorageContext](../StorageContex.md)

Key: clave, tipo string.

Valor devuelto: el valor correspondiente a la clave, byte array.

## Ejemplo

```c#
public class Contract1: FunctionCode
{
     public static void Main ()
     {
         byte[] value = Storage.Get (Storage.CurrentContext, "key");
     }
}
```



[Volver arriba](../Storage.md)
