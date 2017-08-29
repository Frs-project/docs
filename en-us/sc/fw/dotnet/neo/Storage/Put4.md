# Storage.Put Method (StorageContext, string, string)

Inserts a given value to the given key in the persistent store.

Namespace: [FRS.SmartContract.Framework.Services.FRS](../../FRS.md)

Assembly: FRS.SmartContract.Framework

## Syntax

```c#
public extern void Put(FRS.SmartContract.Framework.Services.FRS.StorageContext context, string key, string value)
```

Parameters:

Context: Storage context as a [StorageContext](../StorageContex.md).

Key: Key as a string.

Value: Value as a string.

Return value: void.

## Example

```c#
public class Contract1: FunctionCode
{
     public static void Main()
     {
         String key = "key";
         String value = "value";
         Storage.Put(Storage.CurrentContext, key, value);
     }
}
```



[Back](../Storage.md)