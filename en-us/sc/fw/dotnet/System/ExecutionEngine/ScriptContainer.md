# ExecutionEngine.ScriptContainer Property

Returns the script container of the current contract (The initial trigger). This is usually a transaction, if this contract was triggered by a transaction from a contract account, then the ScriptContainer will be of that transaction. If the current contract was trigger by an Invocation Transaction, then the ScriptContainer will be of that Invocation Transaction's.

Namespace: [FRS.SmartContract.Framework.Services.System](../../System.md)

Assembly: FRS.SmartContract.Framework

## Syntax

```c#
public extern FRS.SmartContract.Framework.IScriptContainer ScriptContainer {get;}
```

Attribute value: ScriptContainer as a IScriptContainer. If you know the trigger is a Transaction, you can cast this into a [Transaction](../../FRS/Transaction.md).



[Back](../ExecutionEngine.md)
