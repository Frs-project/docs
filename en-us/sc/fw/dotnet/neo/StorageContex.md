# StorageContex Class

The class representing the storage context of the persistent store.

The smart contract can obtain its own storage context through Storage.CurrentContext and pass the context as an argument to other contracts(as a way of authorization), allowing other contracts to call the read/write methods for its persistent store.

Note: This is different from the 1.6 version.

Namespace: [FRS.SmartContract.Framework.Services.FRS](../FRS.md)

Assembly: FRS.SmartContract.Framework

## Syntax

```c#
public class StorageContext
```

## Constructor

The StorageContext object is constructed through [Storage.CurrentContext](Storage/CurrentContext.md).
