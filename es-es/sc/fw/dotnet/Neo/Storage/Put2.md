# Método Storage.Put (StorageContext, byte[], string)

Operación de inserción en la forma clave-valor (byte-array, string) en el almacenamiento persistenten.

Namespace: [FRS.SmartContract.Framework.Services.FRS](../../FRS.md)

Assembly: FRS.SmartContract.Framework

## Sintaxis

```c#
public extern void Put (FRS.SmartContract.Framework.Services.FRS.StorageContext context, byte[] key, byte[] value)
```

## Parámetros:

Context: Contexto de almacenamiento, tipo [StorageContext](../StorageContex.md)

Key: clave, byte array.

Value: valor, byte array.

Valor devuelto: void.

## Ejemplo

```c#
public class Contract1: FunctionCode
{
     public static void Main ()
     {
         byte[] key = new byte[] {0};
         String value = "value";
         Storage.Put (Storage.CurrentContext, key, value);
     }
}

```

[Volver arriba](../Storage.md)
