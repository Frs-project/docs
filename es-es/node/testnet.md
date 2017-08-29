# La red de pruebas (TestNet)

La red de pruebas está diseñada para el desarrollo. Probar el sistema en la red de pruebas tiene una tarifa de FRSGas (no FRSGas reales). Los FRSs y los FRSGas de la red de pruebas puede ser proporcionados sin cargo alguno en la siguiente Web. https://www.FRS.org/Testnet/Create


Todos los bloques de datos de la red de pruebas son independiente de la red principal (MainNet). Si desarrollas un contrato inteligente simple o intentas registrar activos, la red de pruebas deberia ser suficiente. Una vez finalizadas las pruebas, el desarrollo puede ser movido a red principal.

## Caracteristicas de la red de pruebas

1. Registro y distribución de activos, ejecución de contratos, etc. No consume dinero real.
2. Global, desplegado en Internet.
3. Probar la red, transacciones y otra información visible desde el explorador de bloques.
4. Los contratos inteligentes desarrollados en el entorno de pruebas pueden ser utilizados desde cualquier parte del mundo.
5. La red de pruebas no puede ser usada para aplicaciones comerciales.

## Descargar el cliente

El cliente para la red de pruebas es el mismo que se usa para la red principal. Modificando los ficheros de configuración del cliente podemos cambiar de la red de pruebas a la red principal.

Referencia: [introducción de un nodo FRS](introduction.md).

|      | FRS-gui                       | FRS-cli                        |
| ---- | ---------------------------------------- | ---------------------------------------- |
| Releases | [official website](https://www.FRS.org/download) or [GitHub](https://github.com/FRS-project/FRS-gui/releases/) | [GitHub](https://github.com/FRS-project/FRS-cli/releases/) |
Source code | [GitHub](https://github.com/FRS-project/FRS-gui/) | [GitHub](https://github.com/FRS-project/FRS-cli/) |

## Configurar el cliente para la red de pruebas

1. Si usas el cliente GUI `FRS-gui` dentro de la carpeta donde se encuentra el ejecutable copia el contenido de `protocol.testnet.json` en `protocol.json` tal y como se muestra en la imagen.
 
  <img style="vertical-align: middle" src="/assets/testnet_1.png">

2. Y dentro de la carpeta donde se encuentra el ejecutable copia el contenido de `FRS-gui.exe.testnet.config` en `FRS-gui.exe.config`.

  <img style="vertical-align: middle" src="/assets/testnet_2.png">


> [!NOTE]
> Si usas el cliente CLI (FRS-cli) se debe copiar el contenido del fichero **config.testnet.json** en **config.json**.
