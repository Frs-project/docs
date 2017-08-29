# FRS node introduction

Full nodes are nodes that store all of the blockchain data. The nodes are connected to the blockchain, through a P2P network. In the blockchain network, all the nodes are equal, where it acts both as a client interface, and as a server.

There are two full-node programs. The first one is for ordinary users, displayed with a graphical user interface and all the basic functions of a user-client. We call it FRS-GUI.

The other is meant to be used by developers, hosted within the command line interface, and provides an external API for most of the basic wallet functions. This node also helps other nodes achieve consensus with the network, and is also involved in the generation of new blocks. We call It FRS-CLI.

Finally, this section also contains information about the FRS [network protocol](network-protocol.md), which provides a low level API for some transaction types that are not currently supported explicity by the CLI, such as claiming GAS or sending FRS without an open wallet. 

## FRS node download address

|      | FRS-GUI                        | FRS-CLI                        |
| ---- | ---------------------------------------- | ---------------------------------------- |
| Releases | [Official website](https://www.FRS.org/download) or [Github](https://github.com/FRS-project/FRS-gui/releases) | [Github](https://github.com/FRS-project/FRS-cli/releases) |
| Source code | [Github](https://github.com/FRS-project/FRS-gui) | [Github](https://github.com/FRS-project/FRS-cli) |

## Comparison of GUI node and CLI node functions

|           | GUI  | CLI  |
| --------- | ---- | ---- |
| Graphic Interface | ✅    |      |
| Command Line Interface |      | ✅    |
| Create Wallet | ✅    | ✅    |
| Open Wallet | ✅    | ✅  |
| Reconstruct Wallet Index | ✅    | ✅    |
| Show all key pairs | ✅    | ✅    |
| Import/Export Key Pair | ✅    | ✅    |
| Show all addresses | ✅    | ✅    |
| Show all assets | ✅    | ✅    |
| Create Address | ✅    | ✅    |
| Transfer | ✅    | ✅    |
| Transaction (Asset swap)  | ✅    |      |
| Create a multi-party signature contract | ✅    |      |
| Create a custom smart contract | ✅    |      |
| Signature | ✅    |      |
| Election Consensus Node | ✅    |      |
| Voting | ✅    |      |
| Register assets | ✅    |      |
| Distribution of assets | ✅    |      |
| Extraction of FRS | ✅    |      |
| Batch Generation Address  |      | ✅    |
| JSON-RPC |      | ✅    |
| The consensus of the participating blocks |      | ✅    |

## Port description

If you want an external program to access the node's API, an open firewall port is required. The following is a port description that can be set to fully open or open-on-demand.

|                    | Main Net | Test Net |
| ------------------ | ------------ | ------------- |
| JSON-RPC via HTTPS | 10331        | 20331         |
| JSON-RPC via HTTP  | 10332        | 20332         |
| P2P via TCP        | 10333        | 20333         |
| P2P via WebSocket  | 10334        | 20334         |

For more information, please refer to [test network](testnet.md).
