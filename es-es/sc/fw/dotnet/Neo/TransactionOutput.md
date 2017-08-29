# Clase TransactionOutput

La estructura de datos usada para representar la salida de la transación. La salida de la transación tiene tres campos:
La transferencia del activo, la direcció y cuanto dinero transferido.

Namespace: [FRS.SmartContract.Framework.Services.FRS](../FRS.md)

Assembly: FRS.SmartContract.Framework

## Sintaxis

```c#
public class TransactionOutput: IApiInterface
```

## Atributos

| | Nombre | Descripción |
| ---------------------------------------- | ---------------------------------------- | ------ |
| [AssetId](TransactionOutput/AssetId.md) | Devuelve el id. del asset |
| [ScriptHash](TransactionOutput/ScriptHash.md) | Devuelve el hash del script | 
| [Value](TransactionOutput/Value.md) | Devuelve la cantidad de tranferida |

## Método de constructor

El objeto TransactionOutput se construye con el metodo [GetOutputs ()](Transaction/GetOutputs.md) del objeto Transaction.


