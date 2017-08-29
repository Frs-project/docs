# Método Storage.Put (StorageContext, string, string)

Operación de inserción en la forma clave-valor (string, string) en el almacenamiento persitente.

Namespace: [FRS.SmartContract.Framework.Services.FRS](../../FRS.md)

Assembly: FRS.SmartContract.Framework

## Sintaxis

```c#
public extern void Put (FRS.SmartContract.Framework.Services.FRS.StorageContext context, string key, string value)
```

## Parámetros

Context: Contexto de almacenamiento, tipo [StorageContext](../StorageContex.md)

Key: clave, string.

Value: valor, string.

Valor devuelto: void.

## Ejemplo

```c#
public class Contract1: FunctionCode
{
     public static void Main ()
     {
         String key = "key";
         String value = "value";
         Storage.Put (Storage.CurrentContext, key, value);
     }
}
```


[Volver arriba](../Storage.md)
