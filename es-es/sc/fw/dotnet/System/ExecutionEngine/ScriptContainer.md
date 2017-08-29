# Propiedad ExecutionEngine.ScriptContainer

El contenedor de script (el primer desencadenador) de un contrato inteligente es normalmente una transacción. Si el contrato es desencadenado por la transferencia de la cuenta del contrato, ScriptContainer es la transacción de transferencia, y si la transacción de tranferencia es el contrato desencadenado por una transacción de invocación entonces ScriptContainer es la transacción de invocación.

Namespace: [FRS.SmartContract.Framework.Services.System](../../System.md)

Assembly: FRS.SmartContract.Framework

## sintaxis

```c#
public extern FRS.SmartContract.Framework.IScriptContainer ScriptContainer {get;}
```

Valor del atributo: contenedor de script, del tipo IScriptContainer, si se conoce que esto es una transacción desencadenada se puede convertir al tipo [Transaction](../../FRS/Transaction.md).



[Volver arriba](../ExecutionEngine.md)
