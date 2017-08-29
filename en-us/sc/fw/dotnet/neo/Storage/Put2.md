# Storage.Put Method (StorageContext, byte[], string)

Inserts a given value to the given key in the persistent store.

Namespace: [FRS.SmartContract.Framework.Services.FRS](../../FRS.md)

Assembly: FRS.SmartContract.Framework

## Syntax

```c#
public extern void Put(FRS.SmartContract.Framework.Services.FRS.StorageContext context, byte[] key, string value)
```

Parameters:

Context: Storage context as a [StorageContext](../StorageContex.md).

Key: Key as a byte array.

Value: Value as a string.

Return value: void.

## Example

```c#
public class Contract1: FunctionCode
{
     public static void Main()
     {
         byte[] key = new byte[] {0};
         String value = "value";
         Storage.Put(Storage.CurrentContext, key, value);
     }
}
```



[Back](../Storage.md)
