# Storage.CurrentContext Property

Returns the current store context. After obtaining the store context, the object can be passed as an argument to other contracts (as a way of authorization), allowing other contracts to perform read/write operations on the persistent store of the current contract.

Note: This is different from the 1.6 version.

Namespace: [FRS.SmartContract.Framework.Services.FRS](../../FRS.md)

Assembly: FRS.SmartContract.Framework

## Syntax

```c#
public static extern FRS.SmartContract.Framework.Services.FRS.StorageContext CurrentContext {get;}
```

Attribute value: Current storage context as a [StorageContext](../StorageContex.md).



[Back](../Storage.md)