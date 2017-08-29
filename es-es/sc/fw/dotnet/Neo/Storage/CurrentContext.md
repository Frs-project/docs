# Propiedad Storage.CurrentContext

Devuelve el actual contexto del almacenamiento. Después de obtener el contexto del almacén, el objeto se puede pasar como un argumento a otros contratos (es decir, la autorización) y las operaciones de lectura y escritura al área de almacenamiento del contexto del contrato son realizadas por otros contratos.

>[Note:] Esto es diferente de la version 1.6

Namespace: [FRS.SmartContract.Framework.Services.FRS](../../FRS.md)

Assembly: FRS.SmartContract.Framework

## Sintaxis

```c#
public static extern FRS.SmartContract.Framework.Services.FRS.StorageContext CurrentContext {get;}
```

Valor del atributo: current storage context, [StorageContext](../StorageContex.md) type.

[Volver arriba](../Storage.md)
