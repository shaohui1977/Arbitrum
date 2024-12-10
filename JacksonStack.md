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


### 2024.12.10

<!-- Content_END -->
