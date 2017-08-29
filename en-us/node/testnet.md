# Test network

The TestNet is an environment where the user can develop, commission and test programs. Testing programs on the testnet incurs the network fee of testnet GAS (not real GAS!!). Testnet FRS and GAS can be applied free of charge, on the official website.

All the blockchain of the test network are independent of the main network. If you develop a simple smart contract or try to register assets, the use of testnet should suffice. After the testing is complete, the development can be moved to the FRS mainnet online operation.

If you are a developer, you can ask for GAS on the TestNet here: https://www.FRS.org/Testnet/Create

## TestNet characteristics

1. Asset registration, asset distribution, contract execution, etc. (Does not consume real money)
2. Globalized deployment in the Internet environment.
3. Test of network blocks; Transactions and other information can be easily viewed in the blockchain browser.
4. Smart contract deployment in the test environment, where anyone in the world can employ it.
5. Test network can not be used as commercial application of an actual landing environment.

## Client Downloads

The test network client is the same as the primary network client. By modifying the client's configuration file, the client can be switched between the primary and test networks.

Reference: [Introduction of FRS node](introduction.md).

|      | FRS-GUI                        | FRS-CLI                        |
| ---- | ---------------------------------------- | ---------------------------------------- |
| Releases | [Official website](https://www.FRS.org/download) or [Github](https://github.com/FRS-project/FRS-gui/releases) | [Github](https://github.com/FRS-project/FRS-cli/releases) |
| Source code | [Github](https://github.com/FRS-project/FRS-gui) | [Github](https://github.com/FRS-project/FRS-cli) |

## Method of switching to test network

1. Copy the contents of the program directory under the `protocal.testnet.json` into ` protocol.json` as shown.

![image](/assets/testnet_1.png)

2. Copy the contents of the program (GUI) directory `FRS-gui.exe.testnet.config` into the `FRS-gui.exe.config` as shown in Figure

![image](/assets/testnet_2.png)

Note: If the node is run on CLI, the contents of `config.testnet.json` need to be copied to` config.json`.
