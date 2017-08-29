# FRS Namespace

The FRS namespace is the API provided by the FRS blockchain, providing a way to access the block-chain data and manipulate the persistent store. These APIs are divided into two categories:

1. Blockchain ledger. The contract can access all the data on the entire blockchain through interops layer, including complete blocks and transactions, as well as each of their fields.

2. Persistent store. Each application contract deployed on FRS has a storage space that can only be accessed by the contract itself. These methods provided can access the data in the contract.

Note: The `New` and `Deprecated` tags in this article are the changes to version 2.0 relative to version 1.6.

## Class

| | Class | Description |
| ---------------------------------------- | ---------------------------------------- | ---------------------- |
| ![](https://i-msdn.sec.s-msft.com/dynimg/IC29808.jpeg) | [Account](FRS/Account.md)          | A class representing the Account, providing a method to query the balance.      |
| ![](https://i-msdn.sec.s-msft.com/dynimg/IC29808.jpeg) | [Asset](FRS/Asset.md)              | A class representing an asset and its data structure.         |
| ![](https://i-msdn.sec.s-msft.com/dynimg/IC29808.jpeg) | [Block](FRS/Block.md)              | A class representing a block, provides methods to query transactions in the block.  |
| ![](https://i-msdn.sec.s-msft.com/dynimg/IC29808.jpeg) | [Blockchain](FRS/Blockchain.md)    | Provides a set of methods for accessing blockchain data.    |
| ![](https://i-msdn.sec.s-msft.com/dynimg/IC29808.jpeg) | [Contract](FRS/Contract.md)        | A class representing a contract.                |
| ![](https://i-msdn.sec.s-msft.com/dynimg/IC29808.jpeg) | [Enrollment](FRS/Enrollment.md)    | `New` Represents the data structure of the registration transaction of a bookkeeper. |
| ![](https://i-msdn.sec.s-msft.com/dynimg/IC29808.jpeg) | [Header](FRS/Header.md)            | Represents the data structure of a block header           |
| ![](https://i-msdn.sec.s-msft.com/dynimg/IC29808.jpeg) | [Runtime](FRS/Runtime.md)          | `New` Provides a set of methods during smart contract execution   |
| ![](https://i-msdn.sec.s-msft.com/dynimg/IC29808.jpeg) | [Storage](FRS/Storage.md)          | Provides a set of methods to insert, query, or delete data of a persistent store   |
| ![](https://i-msdn.sec.s-msft.com/dynimg/IC29808.jpeg) | [StorageContex](FRS/StorageContex.md) | `New` A class representing storage context of the persistent store  |
| ![](https://i-msdn.sec.s-msft.com/dynimg/IC29808.jpeg) | [Transaction](FRS/Transaction.md)  |  The base class representing the transaction            |
| ![](https://i-msdn.sec.s-msft.com/dynimg/IC29808.jpeg) | [TransactionAttribute](FRS/TransactionAttribute.md) | The data structure representing the transaction attributes          |
| ![](https://i-msdn.sec.s-msft.com/dynimg/IC29808.jpeg) | [TransactionInput](FRS/TransactionInput.md) | The data structure representing the transaction inputs         |
| ![](https://i-msdn.sec.s-msft.com/dynimg/IC29808.jpeg) | [TransactionOutput](FRS/TransactionOutput.md) | The data structure representing the transaction outputs         |
| ![](https://i-msdn.sec.s-msft.com/dynimg/IC29808.jpeg) | [Validator](FRS/Validator.md)      | `New` Provides a set of methods for consensus nodes      |

## Enumeration

|  | Enumeration | Description |
| ---------------------------------------- | ---------------------------------------- | ----------------------- |
| ![](https://i-msdn.sec.s-msft.com/dynimg/IC134134.jpeg) | [StorageContex](FRS/StorageContex2.md) | `Deprecated`  Represents the enum of the storage context. |
