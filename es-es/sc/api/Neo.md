# Namespace FRS

El namespace `FRS` es la API proporcionada por la blockchain de FRS, esta facilita el acceso a los datos de la blockchain y la manipulación del almacenamiento persistente. Estas APIs están divididas en dos categorías:

  * API de sólo lectura: Los procedimientos de contrato pueden acceder a través de la API a toda la información de la cadena de bloques, incluyendo los bloques, transacciones, activos así como sus respectivos campos.

  * API de lectura/escritura. A través de estas APIs los contratos inteligentes pueden modificar el estado de los contratos, así como la lectura y escritura en áreas del almacenamiento persistente.

Nota: Las etiquetas `nueva` y `obsoleta` indican los cambios realizados en la versión 2.0 en relación a la 1.6.

## API de sólo lectura

Consulta de datos desde la API de la **Blockchain**:

| API | Descripción |
| ----------------------------------- | -------------------- |
| FRS.Blockchain.GetHeight | Obtiene el tamaño del bloque actual. |
| FRS.Blockchain.GetHeader | Busca la cabecera del bloque por su tamaño o su hash. |
| FRS.Blockchain.GetBlock | Busca bloques por su tamaño o su hash. |
| FRS.Blockchain.GetTransaction | Busca transaciones vía ID de transacción. |
| FRS.Blockchain.GetAccount | Obtiene una cuenta basada en el hash del script del contrato. |
| FRS.Blockchain.GetValidators | `nueva` Obtiene la clave pública de la persona de consenso. |
| FRS.Blockchain.GetAsset | Busca activos basados en un id. de activo. |
| FRS.Blockchain.GetContract | `nueva` Obtiene el contenido del contrato basado en un hash de contrato. |

API de la clase **Block**:

| API | Descripción |
| ----------------------------------- | -------------------------- |
| FRS.Header.GetHash | Obtiene el hash del bloque. |
| FRS.Header.GetVersion | Obtiene el número de versión del bloque. |
| FRS.Header.GetPrevHash | Obtiene el hash del bloque previo. |
| FRS.Header.GetMerkleRoot | Obtiene la raíz del árbol Merkle para todas las transacciones de ese bloque. |
| FRS.Header.GetTimestamp | Obtiene el timestamp del bloque.
| FRS.Header.GetConsensusData | Obtiene los datos de consenso del bloque. (consensus node-generated pseudo-random number) |
| FRS.Header.GetNextConsensus | Obtiene el valor hash para el siguiente contrato. |
| FRS.Block.GetTransactionCount | Obtiene el número de transacciones del bloque actual. |
| FRS.Block.GetTransactions | Obtiene todas las transacciones del bloque actual. |
| FRS.Block.GetTransaction | Obtiene la transacción especificada en el bloque actual. |

API de la clase **Transaction:**

| API | Descripción |
| ----------------------------------- | ---------------------------------------- |
| FRS.Transaction.GetHash | Obtiene el hash para la transacción actual.
| FRS.Transaction.GetType | Obtiene el tipo de la transacción actual. |
| FRS.Enrollment.GetPublicKey | `obsoleta` reemplazada por `FRS.Blockchain.GetValidators`. |
| FRS.Transaction.GetAttributes | Consulta todas las propiedades de la transacción actual. |
| FRS.Transaction.GetInputs | Consulta todas las transacciones para la transacción actual. |
| FRS.Transaction.GetOutputs | Consulta todas las salidas de la transacción actual. |
| FRS.Transaction.GetReferences | Consulta la transacción de salida referenciada por todas las entradas de la transacción actual. |
| FRS.Attribute.GetUsage | Obtiene datos adicionales de la transación. |
| FRS.Attribute.GetData | Obtiene datos adicionales de la transación. |
| FRS.Input.GetHash | La transación que hace referencia en la transación. |
| FRS.Input.GetIndex | Índice de la transacción referenciada en su lista de transacciones de salida. |
| FRS.Output.GetAssetId | Obtiene el ID del activo. |
| FRS.Output.GetValue | Obtiene el hash del script. |
| FRS.Output.GetScriptHash | Obtiene el total de la transacción. |

API de la clase **Account:**

| API | Descripción |
| ------------------------------- | ------------------ |
| FRS.Account.GetScriptHash | Obtiene el hash del script de la cuenta del contrato. |
| FRS.Account.GetVotes | Permite a terceros ver la información de votación para la cuenta del contrato. |
| FRS.Account.GetBalance | Obtiene el importe del activo de la cuenta dado un ID de activo. |

API de la clase **Asset:**

| API | Descripción |
| ---------------------------- | ------------------------------------- |
| FRS.Asset.GetAssetId | Obtiene el ID del activo. |
| FRS.Asset.GetAssetType | Obtiene la categoría del activo. |
| FRS.Asset.GetAmount | Obtiene el importe total del activo. |
| FRS.Asset.GetAvailable | Obtiene la cantidad de activo que ha sido emitido. |
| FRS.Asset.GetPrecision | Obtiene la precisión del activo (número mínimo de divisiones), el número de decimales después de la coma. |
| FRS.Asset.GetOwner | Obtiene el propietario del activo. (clave pública) |
| FRS.Asset.GetAdmin | Obtiene el administrador (dirección del contrato) del activo y el derecho a modificar sus atributos. (como el total, nombre, etc.) |
| FRS.Asset.GetIssuer | Obtiene el emisor (dirección del contrato) del activo y el derecho a emitir el activo. |

API de la clase **Contract:**

| API | Descripción |
| ---------------------------- | -------- |
| FRS.Contract.GetScript | Obtiene el script para el contrato. |

API de la clase **Storage:**

| API | Descripción |
| ---------------------------- | ------------------------------- |
| FRS.Storage.GetContext | `nueva` Obtiene el contexto de almacenamiento actual. |
| FRS.Storage.Get | operación de consulta en el área de almacenamiento persistente, obtiene el valor correspondiente a una consulta por su clave. |

## API de lectura/escritura

Este tipo de API modifica el estado del contrato inteligente.

| API | Descripción |
| -------------------------------------- | -------------------------------- |
| FRS.Blockchain.RegisterValidator | `nueva` Registrarse como contador. |
| FRS.Blockchain.CreateAsset | `nuevo` Registrar un activo. |
| FRS.Blockchain.CreateContract | `nuevo` Anuncia un contrato inteligente. |
| FRS.Account.SetVotes | Estable votos para la cuenta contrato a otras personas. |
| FRS.Asset.Renew | `nuevo` Renovación de activo. |
| FRS.Contract.Destroy | `nuevo` Destruye el contrato. |
| FRS.Storage.Put | Operación de inserción, inserta datos del tipo clave-valor dentro del área de almacenamiento persistente. |
| FRS.Storage.Delete | Operación de eliminación, elimina del área de almacenamiento persistente un valor dada su clave. |
