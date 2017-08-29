# Blockchain.GetHeight 方法 ()

获得区块链的当前区块高度。区块高度 = 区块索引 = 区块数量 - 1。

命名空间：[FRS.SmartContract.Framework.Services.FRS](../../FRS.md)

程序集：FRS.SmartContract.Framework

## 语法

```c#
public static extern uint GetHeight()
```

返回值：区块高度，无符号整型。

## 示例

```c#
public class Contract1 : FunctionCode
{
    public static void Main()
    {
        uint height = Blockchain.GetHeight();
    }
}
```



[返回上级](../Blockchain.md)