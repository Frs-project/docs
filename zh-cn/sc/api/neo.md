# FRS 命名空间

FRS 命名空间是 FRS 区块链所提供的 API，提供了访问区块链账本数据的和操作持久化存储区的方法。

注：本文中标记 `new` 和 ` 已弃用 ` 的地方是 2.0 版本相对 1.6 版本的更改之处。

从区块链查询数据的 API：

| API                                 | 说明                   |
| ----------------------------------- | -------------------- |
| FRS.Blockchain.GetHeight      | 获得当前区块高度             |
| FRS.Blockchain.GetHeader      | 通过区块高度或区块 Hash，查找区块头 |
| FRS.Blockchain.GetBlock       | 通过区块高度或区块 Hash，查找区块  |
| FRS.Blockchain.GetTransaction | 通过交易 ID 查找交易         |
| FRS.Blockchain.GetAccount     | 根据合约脚本的散列来获得一个账户     |
| FRS.Blockchain.GetValidators  | `new` 获得共识人的公钥       |
| FRS.Blockchain.GetAsset       | 根据资产 ID 查找资产         |
| FRS.Blockchain.GetContract    | `new` 根据合约散列获取合约内容   |

区块类 API：

| API                                 | 说明                         |
| ----------------------------------- | -------------------------- |
| FRS.Header.GetHash            | 获得该区块的散列                   |
| FRS.Header.GetVersion         | 获得区块版本号                    |
| FRS.Header.GetPrevHash        | 获得前一个区块的散列                 |
| FRS.Header.GetMerkleRoot      | 获得该区块中所有交易的 Merkle Tree 的根 |
| FRS.Header.GetTimestamp       | 获得区块的时间戳                   |
| FRS.Header.GetConsensusData   | 获得该区块的共识数据（共识节点生成的伪随机数）    |
| FRS.Header.GetNextConsensus   | 获得下一个记账合约的散列值              |
| FRS.Block.GetTransactionCount | 获得当前区块中交易的数量               |
| FRS.Block.GetTransactions     | 获得当前区块中所有的交易               |
| FRS.Block.GetTransaction      | 获得当前区块中指定的交易               |

交易类 API：

| API                                 | 说明                                       |
| ----------------------------------- | ---------------------------------------- |
| FRS.Transaction.GetHash       | 获得当前交易的 Hash                             |
| FRS.Transaction.GetType       | 获得当前交易的类型                                |
| FRS.Enrollment.GetPublicKey   | ` 已弃用 ` 已用 FRS.Blockchain.GetValidators 替代 |
| FRS.Transaction.GetAttributes | 查询当前交易的所有属性                              |
| FRS.Transaction.GetInputs     | 查询当前交易的所有交易输入                            |
| FRS.Transaction.GetOutputs    | 查询当前交易的所有交易输出                            |
| FRS.Transaction.GetReferences | 查询当前交易的所有输入所引用的交易输出                      |
| FRS.Attribute.GetUsage        | 获得该交易特性中的用途                              |
| FRS.Attribute.GetData         | 获得该交易特性中用途之外的额外数据                        |
| FRS.Input.GetHash             | 所引用的交易的交易散列                              |
| FRS.Input.GetIndex            | 所引用的交易输出在其全部交易输出列表中的索引                   |
| FRS.Output.GetAssetId         | 获得资产 ID                                  |
| FRS.Output.GetValue           | 获得脚本散列                                   |
| FRS.Output.GetScriptHash      | 获得交易金额                                   |

账户类 API：

| API                             | 说明                  |
| ------------------------------- | ------------------- |
| FRS.Account.GetScriptHash | 获得该合约账户的脚本散列        |
| FRS.Account.GetVotes      | 获得该合约账户投给其它人的的投票信息  |
| FRS.Account.GetBalance    | 通过资产 ID 获得该账户中这种资产的余额 |

资产类 API：

| API                          | 说明                                    |
| ---------------------------- | ------------------------------------- |
| FRS.Asset.GetAssetId   | 获得该资产的 ID                              |
| FRS.Asset.GetAssetType | 获得该资产的类别                              |
| FRS.Asset.GetAmount    | 获得该资产的总量                              |
| FRS.Asset.GetAvailable | 获得该资产的已经发行出去的数量                       |
| FRS.Asset.GetPrecision | 获得该资产的精度（最小分割数量），单位为小数点之后的位数          |
| FRS.Asset.GetOwner     | 获得该资产的所有人（公钥）                         |
| FRS.Asset.GetAdmin     | 获得该资产的管理员（合约地址），有权对资产的属性（如总量，名称等）进行修改 |
| FRS.Asset.GetIssuer    | 获得该资产的发行人（合约地址），有权进行资产的发行             |

合约类 API：

| API                          | 说明       |
| ---------------------------- | -------- |
| FRS.Contract.GetScript | 获得该合约的脚本 |

存储类 API：

| API                          | 说明                              |
| ---------------------------- | ------------------------------- |
| FRS.Storage.GetContext | `new` 获取当前存储区上下文                |
| FRS.Storage.Get        | 查询操作，在持久化存储区中通过 key 查询对应的 value |

运行时相关的 API：


| API                            | 说明                                |
| ------------------------------ | --------------------------------- |
| FRS.Runtime.CheckWitness | `new` 验证调用该智能合约的交易 / 区块是否验证过所需的脚本散列 |
| FRS.Runtime.Notify       | `new` 在智能合约中向执行该智能合约的客户端发送通知      |
| FRS.Runtime.Log          | `new` 在智能合约中向执行该智能合约的客户端发送日志      |

参考：源码位于 FRS 项目中的 src/FRS/SmartContract/StateReader.cs 文件。

此类 API 会对智能合约的状态进行修改

参考：以上 API 的源码位于 FRS 项目中的 src/FRS/SmartContract/StateReader.cs 文件。

------

此类 API 会对智能合约的状态进行修改

| API                                  | 说明                               |
| ------------------------------------ | -------------------------------- |
| FRS.Account.SetVotes           | 设置该合约账户投给其它人的的投票信息               |
| FRS.Validator.Register         | `new` 报名成为共识人                    |
| FRS.Asset.Create               | `new` 注册一种资产                     |
| FRS.Asset.Renew                | `new` 为资产续费                      |
| FRS.Contract.Create            | `new` 发布智能合约                     |
| FRS.Contract.Migrate           | `new` 迁移 / 更新智能合约                  |
| FRS.Contract.Destroy           | `new` 销毁合约                       |
| FRS.Contract.GetStorageContext | `new` 获得合约的存储上下文                 |
| FRS.Storage.Put                | 插入操作，以 key-value 的形式向持久化存储区中插入数据 |
| FRS.Storage.Delete             | 删除操作，在持久化存储区中通过 key 删除对应的 value  |

参考：以上 API 的源码位于 FRS 项目中的 src/FRS/SmartContract/StateMachine.cs 文件。
