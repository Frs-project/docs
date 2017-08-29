# Método Storage.Put (StorageContext, string, byte[])

Operación de inserción en la forma clave-valor (string,byte-array) en el almacenamiento persitente.

Namespace: [FRS.SmartContract.Framework.Services.FRS](../../FRS.md)

Assembly: FRS.SmartContract.Framework

## Sintaxis

```c#
public extern void Put (FRS.SmartContract.Framework.Services.FRS.StorageContext context, string key, byte[] value)
```

## Parámetros:

Context: Contexto de almacenamiento, tipo [StorageContext](../StorageContex.md)

Key: clave, string.

Value: valor, byte array.

Valor devuelto: void.

## Ejemplo

```c#
public class Contract1: FunctionCode
{
     public static void Main ()
     {
         String key = "key";
         byte[] value = new byte[] {1};
         Storage.Put (Storage.CurrentContext, key, value);
     }
}
```


[Volver arriba](../Storage.md)
