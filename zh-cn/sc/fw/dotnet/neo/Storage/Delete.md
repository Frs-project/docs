# Storage.Delete 方法 (StorageContext, byte[])

删除操作，在持久化存储区中通过 key 删除对应的 value。

命名空间：[FRS.SmartContract.Framework.Services.FRS](../../FRS.md)

程序集：FRS.SmartContract.Framework

## 语法

```c#
public extern void Delete(FRS.SmartContract.Framework.Services.FRS.StorageContext context, byte[] key)
```

参数：
​	context：存储上下文，[StorageContext](../StorageContex.md) 类型。

​	key：键，字节数组。

返回值：void。

## 示例

```c#
public class Contract1 : FunctionCode
{
    public static void Main()
    {
        Storage.Delete(Storage.CurrentContext, new byte[] { 0 });
    }
}
```



[返回上级](../Storage.md)