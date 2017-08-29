# Storage.Get Method (StorageContext, string)

Returns a value from the persistent store based on the given key.

Namespace: [FRS.SmartContract.Framework.Services.FRS](../../FRS.md)

Assembly: FRS.SmartContract.Framework

## Syntax

```c#
public extern byte[] Get(FRS.SmartContract.Framework.Services.FRS.StorageContext context, string key)
```

Parameters:

Context: Storage context as a [StorageContext](../StorageContex.md).

Key: Key as a string.

Return Value: The value corresponding to the key as a byte array.

## Example

```c#
public class Contract1: FunctionCode
{
     public static void Main()
     {
         byte[] value = Storage.Get(Storage.CurrentContext, "key");
     }
}
```



[Back](../Storage.md)
