# Storage.Delete Method (StorageContext, byte[])

Deletes a value from the peristent store based on the given key.

Namespace: [FRS.SmartContract.Framework.Services.FRS](../../FRS.md)

Assembly: FRS.SmartContract.Framework

## Syntax

```c#
public extern void Delete(FRS.SmartContract.Framework.Services.FRS.StorageContext context, byte[] key)
```

Parameters:

Context: Storage context as a [StorageContext](../StorageContex.md).

Key: Key as a byte array.

Return value: void.

## Example

```c#
public class Contract1: FunctionCode
{
     public static void Main()
     {
         Storage.Delete(Storage.CurrentContext, new byte[] {0});
     }
}
```



[Back](../Storage.md)