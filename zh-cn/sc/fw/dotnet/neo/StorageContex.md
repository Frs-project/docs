# StorageContex 类

用来表示私有存储区存储上下文的类。

在智能合约中可以通过 Storage.CurrentContext 获得自己的存储区上下文，之后可以将该对象作为实参传给其它合约（即完成授权），由其它合约来执行对该合约上下文的存储区的读写操作。

注：此处与 1.6 版本有所不同。

命名空间：[FRS.SmartContract.Framework.Services.FRS](../FRS.md)

程序集：FRS.SmartContract.Framework

## 语法

```c#
public class StorageContext
```

## 构造方法

通过 [Storage.CurrentContext](Storage/CurrentContext.md) 属性来构造 StorageContext 对象。