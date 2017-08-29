# StorageContex 枚举

用来表示私有存储区存储上下文的枚举。

> [!Caution]
> 注：在 2.0 版本中已经弃用。

命名空间：[FRS.SmartContract.Framework.Services.FRS](../FRS.md)

程序集：FRS.SmartContract.Framework

## 语法

```c#
public enum StorageContext : byte
```

## 枚举

|                                          | 名称                                       | 说明                     |
| ---------------------------------------- | ---------------------------------------- | ---------------------- |
| ![](https://i-msdn.sec.s-msft.com/dynimg/IC134134.jpeg) | [CallingContract](StorageContex/CallingContract.md) | 调用者的存储上下文              |
| ![](https://i-msdn.sec.s-msft.com/dynimg/IC134134.jpeg) | [Current](StorageContex/Current.md)      | 当前合约的存储上下文             |
| ![](https://i-msdn.sec.s-msft.com/dynimg/IC134134.jpeg) | [EntryContract](StorageContex/EntryContract.md) | 合约入口点（合约调用链的起始点）的存储上下文 |

