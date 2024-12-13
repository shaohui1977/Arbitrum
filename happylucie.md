---
timezone: Asia/Shanghai
---

# {Lucie}

1. 程序员，社区新人，第一次参加这样的学习活动，非常期待！
2. 可以的，不懂就问

## Notes

<!-- Content_START -->

### 2024.12.10


<!-- Content_END -->
---
timezone: Asia/Shanghai
---

# {Lucie}

1. 程序员，社区新人，第一次参加这样的学习活动，非常期待！
2. 可以的，不懂就问

## Notes

<!-- Content_START -->

### 2024.12.10
#### Why Arbitrum?
以太坊如果想真正去中心化，就应该reasonably accessible for anyone。
所以，交易吞吐量注定不能太大。

#### What's Arbitrum?
以太坊扩展解决方案套件，使得部署和使用去中心化应用更加容易。
**Arbitrum Rollup**	A protocol for scaling Ethereum smart contracts.
**Arbitrum AnyTrust** A protocol for scaling Ethereum smart contracts even further, with a mild trust assumption.
**Arbitrum Nitro**	The node software that codifies the Rollup and AnyTrust protocols.
**Arbitrum nodes**	Machines that run Nitro in order to service and/or interact with an Arbitrum chain.
**Arbitrum One**	A public Rollup chain.
**Arbitrum Nova**	A public AnyTrust chain.
**Arbitrum bridge**	Let you move ETH and ERC-20 tokens between Ethereum, Arbitrum, and select Orbit chains.
**Arbitrum Orbit**	Let you run your own Rollup and AnyTrust chains.
**Arbitrum Stylus**	Let you write EVM-compatible smart contracts in Rust and any other language that compiles to Wasm.

**核心特点**
1. 优化的扩展性
通过将大部分交易计算和数据存储移至 Layer 2，减轻以太坊主网的负担。
支持数千笔每秒的交易，而主网的吞吐量仅为数十笔。
2. 低费用的同时保证安全性
大幅降低了用户的交易成本，同时利用以太坊主网作为最终的安全保障层，任何争议都可以在以太坊主链上解决。
3. 与以太坊的高兼容性
兼容以太坊虚拟机（EVM），开发者无需修改代码即可部署现有的以太坊智能合约。
支持以太坊钱包和工具（如 MetaMask、Hardhat）。
4. 多链支持与灵活选择
Arbitrum 支持多条链并行运行。在以太坊主网上，有2条 Arbitrum 链：一条 Arbitrum Rollup 链，称为**Arbitrum One**，一条 AnyTrust链，称为**Nova**;用户和开发人员可以选择适合他们的安全/交易成本需求的任何选项。

**Optimistic Rollup**
乐观验证：默认情况下，Rollup 假设所有提交的交易都是有效的。如果有人发现有欺诈行为，可以发起挑战，系统会进行验证和纠正。
链下计算：大部分计算和数据处理在链下完成，仅将必要的数据和交易摘要提交到以太坊主链，大大减少了链上负载。


### 2024.12.11
**Op Rollups 与 ZK Rollups**
1. ZK 所有人都能通过 PoW 认证来参与认证
2. OP 更倾向于选择一组值得信赖的认证者，监督整个打包交易的过程

**欺诈证明**
欺诈证明是一种加密和协议机制，旨在在区块链系统中防止和处理潜在的错误或恶意行为。它通过允许参与者对某些不正确的计算结果提出挑战，并验证这些挑战是否成立，从而保护系统的安全性。

在 Arbitrum 中：
验证者提交交易的状态更新，如果其他验证者认为该状态更新不正确，他们可以生成欺诈证明来挑战这一更新。
验证机制会审查这一挑战，通过重新执行部分计算来验证谁是正确的

交互式欺诈证明的执行流程：
1. 断言提交
验证者（Proposer）在 Layer 1 上提交一个状态更新（即 Layer 2 的断言），描述交易如何从一个状态转移到另一个状态。
断言包括起始状态、最终状态，以及该状态转移的证明。
2. 发起挑战
如果另一验证者（Challenger）认为断言不正确，他们可以发起挑战，启动交互式欺诈证明过程。
挑战者的目标是证明某个具体步骤的计算是错误的。
3. 争议分解
二分法定位错误：
争议解决协议将整个断言的计算过程分解为多个步骤。
验证者和挑战者在 Layer 1 上交互，通过多轮的二分查找逐步缩小争议范围，直到定位到一个具体的计算步骤。
每次交互中，双方需要提交关于哪个部分计算是正确的声明，协议将持续缩小范围。
4. 单步验证
一旦缩小到单个计算步骤，系统会在 Layer 1 上重新执行这一步骤。大部分争议分解过程发生在L2链下，只有最终验证单步计算时才在 Layer 1 上执行
如果断言中的该步骤正确，则挑战失败，挑战者被罚款。
如果该步骤错误，则挑战成功，验证者被罚款，断言被撤销。

### 2024.12.12
Arbitrum 详解 - One、Nitro、Nova
https://community.dorahacks.io/t/arbitrum-one-nitro-nova/562
<!-- Content_END -->
