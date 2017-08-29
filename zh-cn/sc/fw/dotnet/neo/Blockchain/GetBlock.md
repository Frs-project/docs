# Blockchain.GetBlock 方法 (byte[])

通过区块高度，在区块链中查找该区块。

命名空间：[FRS.SmartContract.Framework.Services.FRS](../../FRS.md)

程序集：FRS.SmartContract.Framework

## 语法

```c#
public static extern FRS.SmartContract.Framework.Services.FRS.Block GetBlock(byte[] hash)
```

参数：区块 Hash，32字节的字节数组。

返回值：区块，[Block](../Block.md) 类型。

## 示例

```c#
public class Contract1 : FunctionCode
{
    public static void Main()
    {
        byte[] block = new byte[] { 206, 240, 165, 25, 76, 228, 58, 100, 117, 184, 213, 171, 61, 96, 34, 234, 129, 116, 60, 232, 71, 11, 231, 143, 195, 123, 5, 190, 250, 182, 14, 152 };
        Block bl = Blockchain.GetBlock(block);
    }
}
```



[返回上级](../Blockchain.md)