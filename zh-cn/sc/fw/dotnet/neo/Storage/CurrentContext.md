# Storage.CurrentContext 属性

获取当前存储区上下文。获得该存储区上下文后，可以将该对象作为实参传给其它合约（即完成授权），由其它合约来执行对该合约上下文的存储区的读写操作。

注：此处与 1.6 版本有所不同。

命名空间：[FRS.SmartContract.Framework.Services.FRS](../../FRS.md)

程序集：FRS.SmartContract.Framework

## 语法

```c#
public static extern FRS.SmartContract.Framework.Services.FRS.StorageContext CurrentContext { get; }
```

属性值：当前存储区上下文，[StorageContext](../StorageContex.md) 类型。



[返回上级](../Storage.md)