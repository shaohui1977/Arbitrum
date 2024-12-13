---
timezone: Asia/Shanghai
---

# Kylin

1. 自我介绍<br>
web3开发新手；从hackquest了解到Ethereum，Solana，Arbitrum的开发；对Layer2更感兴趣。
2. 你认为你会完成本次残酷学习吗？<br>
  Y
## Notes

<!-- Content_START -->

### 2024.12.10
**What:**<br>
Arbitrum 是一套旨在扩展以太坊的技术方案，允许用户以更低的费用和更快的速度执行在以太坊上的操作，如使用 Web3 应用和部署智能合约。<br>
Arbitrum 的旗舰产品是 Arbitrum Rollup，一个继承了以太坊安全性的 Optimistic Rollup 协议。<br>

**Why:**<br>
以太坊本身的交易处理能力有限，每秒只能处理大约 20-40 笔交易（TPS），导致用户在交易量高峰时需要竞争交易被打包的机会，从而推高了交易费用。<br>

**How:**<br>
 Arbitrum Rollup 链作为以太坊的一个子模块运行，不要求以太坊节点处理每笔 Arbitrum 交易，而是采用“乐观假设”机制，即默认 Arbitrum 上的活动遵循规则，除非有人提出异议。在争议中，两个验证者通过一个交互式的游戏来缩小争议到一个单一的计算步骤，该步骤在 L1 上执行，以证明诚实方说的是真话。<br>
Arbitrum Rollup 链的数据直接发布在以太坊上，确保了安全性和透明度。交易数据以压缩形式发布在 L1 上，进一步减少了交易的 L1 占用空间。<br>
Arbitrum 强调与以太坊的兼容性，用户可以使用他们喜欢的以太坊钱包，开发者可以使用他们喜欢的以太坊库和工具来构建和部署合约。Arbitrum 使用 Geth 的分叉（Nitro）来实现这一点，使得 Arbitrum 中运行的大部分代码与以太坊相同。<br>
Arbitrum 的最新技术堆栈 Stylus 保持了 Nitro 的以太坊兼容性，并增加了新功能，如使用 Rust、C++ 等编程语言编写高性能智能合约的能力。<br>
对于不需要完全去中心化的应用程序，Arbitrum 提供了 AnyTrust 链，这种链在正常情况下将数据保存在链下，只有在争议发生时才会回到“rollup模式”，这样可以显著降低用户的费用。<br>
 Arbitrum 技术支持多条链并行运行，目前以太坊主网上有两条 Arbitrum 链：Arbitrum One（Rollup 链）和 Nova（AnyTrust 链），用户和开发者可以根据他们的安全和交易成本需求选择。<br>


### 2024.12.11
Arbitrum 提供了多种 Layer 2 解决方案，以提高以太坊的可扩展性和降低交易成本：<br>

**Arbitrum One:**<br>
- Optimistic Rollup：通过在链下执行交易并仅将交易数据发布到以太坊主链上，实现高吞吐量。<br>
- Nitro 升级：引入 WASM 和 Geth，优化交易批处理和压缩，提升性能和降低成本。<br>


**Arbitrum Nova：**<br>
  AnyTrust 技术：依赖数据可用性委员会管理链下数据，减少信任需求，提高用户体验，省去了长时间的提币等待期。
  
**Arbitrum Stylus：**<br>
新编程环境：支持使用 Rust、C++ 等语言开发智能合约，增强性能。<br>

**Arbitrum Orbit：**<br>
自定义专用链：允许创建具有自定义隐私、权限和费用代币的专用链。<br>


### 2024.12.12
#### Rollup
Rollup是一种技术，用于提高以太坊网络的交易处理能力（TPS）和降低交易成本。它通过将多笔交易在链下（Layer 2）进行批量处理，然后将结果（压缩数据）发布回以太坊主链（Layer 1）。这样可以减少主链的负担，提高效率。<br>

#### ZK Rollups
ZK Rollups（Zero Knowledge Rollups）是一种使用零知识证明技术的Rollup方案。它允许在Layer 2上进行交易验证，而无需将所有交易数据发布到主链。<br>
零知识证明允许验证者在不透露交易细节的情况下验证交易的有效性。
ZK Rollups的特点包括：
- Zero Knowledge：验证者无需看到交易所有数据。
- Succinct：数据简洁。
- Non-Interactive：无需知道验证者是谁。
- Argument of Knowledge：证明交易的真实性与正确性。

ZK Rollups适合需要快速结算的业务，如支付和交易所，但算法复杂，对应用开发有一定门槛。

#### Optimistic Rollups
Optimistic Rollups是一种Rollup方案，它默认所有交易都是有效的，除非有人提出异议。如果有人发现欺诈行为，可以通过挑战机制来解决。<br>
Optimistic Rollups的特点包括：
- 乐观假设：默认所有交易都是有效的。
- 挑战机制：如果发现问题，可以通过挑战来解决。

Optimistic Rollups适合开发Dapp和DeFi应用，但提币回Layer 1的速度较慢。

#### Arbitrum
Arbitrum是一种基于Optimistic Rollups的Layer 2协议，它通过多轮欺诈证明来增强安全性，并拥有自己的虚拟机，更加兼容以太坊网络。<br>
Arbitrum与Optimism的主要区别在于它进行多轮欺诈证明，并且交易计算不依赖Layer 1。


<!-- Content_END -->
