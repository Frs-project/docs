# Storage.Delete Method (StorageContext, string)

Deletes a value from the peristent store based on the given key.

Namespace: [FRS.SmartContract.Framework.Services.FRS](../../FRS.md)

Assembly: FRS.SmartContract.Framework

## Syntax

```c#
public extern void Delete(FRS.SmartContract.Framework.Services.FRS.StorageContext context, byte[] key)
```

Parameters:

Context: Storage context as a [StorageContext](../StorageContex.md).

Key: Key as a string.

Return value: void.

## Example

```c#
public class Contract1: FunctionCode
{
     public static void Main()
     {
         Storage.Delete(Storage.CurrentContext, "Key");
     }
}
```



[Back](../Storage.md)