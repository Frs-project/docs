# ExecutionEngine.ScriptContainer 属性

获得该智能合约的脚本容器（最开始的触发者），通常是一笔交易，如果该合约是被合约账户转账来触发的，那 ScriptContainer 便是该转账交易，如果该合约是被 Invocation Transaction 来触发的话，那那 ScriptContainer 便是该 Invocation Transaction 交易。

命名空间：[FRS.SmartContract.Framework.Services.System](../../System.md)

程序集：FRS.SmartContract.Framework

## 语法

```c#
public extern FRS.SmartContract.Framework.IScriptContainer ScriptContainer { get; }
```

属性值：脚本容器，IScriptContainer 类型，如果你明确知道它是一笔交易触发的，则可以将其转成 [Transaction](../../FRS/Transaction.md) 类型。



[返回上级](../ExecutionEngine.md)