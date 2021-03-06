# Header Class

Represents the data structure of the block header.

Namespace: [FRS.SmartContract.Framework.Services.FRS](../FRS.md)

Assembly: FRS.SmartContract.Framework

## Syntax

```c#
public class Header: IScriptContainer
```

## Attributes

| | Name | Description |
| ---------------------------------------- | ---------------------------------------- | -------------------------- |
| ![](https://i-msdn.sec.s-msft.com/dynimg/IC74937.jpeg) | [ConsensusData](Header/ConsensusData.md) | Returns the consensus data for the block (generated by the consensus nodes) |
| ![](https://i-msdn.sec.s-msft.com/dynimg/IC74937.jpeg) | [Hash](Header/ConsensusData.md)          | Returns the block hash |
| ![](https://i-msdn.sec.s-msft.com/dynimg/IC74937.jpeg) | [MerkleRoot](Header/MerkleRoot.md)       | Returns the Merkle Tree root for all the transaction in the block |
| ![](https://i-msdn.sec.s-msft.com/dynimg/IC74937.jpeg) | [NextConsensus](Header/NextConsensus.md) | Returns the hash of the next bookeeper |
| ![](https://i-msdn.sec.s-msft.com/dynimg/IC74937.jpeg) | [PrevHash](Header/PrevHash.md)           | Returns the hash of the previous block |
| ![](https://i-msdn.sec.s-msft.com/dynimg/IC74937.jpeg) | [Timestamp](Header/Timestamp.md)         | Returns the timestamp of the block |
| ![](https://i-msdn.sec.s-msft.com/dynimg/IC74937.jpeg) | [Version](Header/Version.md)             | Returns the version of the block  |

## Constructor

The Header object is constructed through [Blockchain.GetHeader(byte[])](Blockchain/GetHeader.md).

The Header object is constructed through [Blockchain.GetHeader(uint)](Blockchain/GetHeader2.md).
