timezone
Asia/Shanghai
请在上边的 timezone 添加你的当地时区，这会有助于你的打卡状态的自动化更新，如果没有添加，默认为北京时间 UTC+8 时区 时区请参考以下列表，请移除 # 以后的内容

timezone: Pacific/Honolulu # 夏威夷-阿留申标准时间 (UTC-10)

timezone: America/Anchorage # 阿拉斯加标准时间 (UTC-9)

timezone: America/Los_Angeles # 太平洋标准时间 (UTC-8)

timezone: America/Denver # 山地标准时间 (UTC-7)

timezone: America/Chicago # 中部标准时间 (UTC-6)

timezone: America/New_York # 东部标准时间 (UTC-5)

timezone: America/Halifax # 大西洋标准时间 (UTC-4)

timezone: America/St_Johns # 纽芬兰标准时间 (UTC-3:30)

timezone: America/Sao_Paulo # 巴西利亚时间 (UTC-3)

timezone: Atlantic/Azores # 亚速尔群岛时间 (UTC-1)

timezone: Europe/London # 格林威治标准时间 (UTC+0)

timezone: Europe/Berlin # 中欧标准时间 (UTC+1)

timezone: Europe/Helsinki # 东欧标准时间 (UTC+2)

timezone: Europe/Moscow # 莫斯科标准时间 (UTC+3)

timezone: Asia/Dubai # 海湾标准时间 (UTC+4)

timezone: Asia/Kolkata # 印度标准时间 (UTC+5:30)

timezone: Asia/Dhaka # 孟加拉国标准时间 (UTC+6)

timezone: Asia/Bangkok # 中南半岛时间 (UTC+7)

timezone: Asia/Shanghai # 中国标准时间 (UTC+8)

timezone: Asia/Tokyo # 日本标准时间 (UTC+9)

timezone: Australia/Sydney # 澳大利亚东部标准时间 (UTC+10)

timezone: Pacific/Auckland # 新西兰标准时间 (UTC+12)

Marcus
hi, 大家好。我是 Marcus,在负责 OP 中文力量，在 Optimism 的研究中，也看到了 arbitrum 的很多治理研究和机制，我想系统的学习一下 arbitrum，这样子便于交流和了解，互相学习

## 2024.12.10
### 简单概念
Arbitrum 是一个 Layer2 网络，用的是 Arbitrum Rollup 的机制（俗称欺诈证明，即代表如果你的交易内有欺诈交易，只要你被证明是虚伪交易，那么你质押的一半资产要给到挑战者）

### 为什么 L2 比 L1 的 Tps 要快很多
其实这点我理解下来比较简单，L2 相当于对交易进行打包，一个包里面包含数百上千笔交易，每次 L1 只处理一个包，这样的效率就提升了几百上千倍，这样子 L2 的 Tps 就会高很多，并且 L2 的共识层也没有改变，还是 L1

### Arbitrum 的兼容性如何
Arbitrum 的创建以以太坊兼容性为首要任务。这意味着用户可以将 Arbitrum 与所有他们喜欢的以太坊钱包一起使用；开发人员可以使用所有他们喜欢的以太坊库和工具构建和部署合约；事实上，大多数时候，使用 Arbitrum 的体验与使用以太坊的体验相同（重要的一点是它更便宜、更快）。

为了实现这种程度的以太坊兼容性，我们进行了大量开发。但其核心是：Arbitrum 本身使用了Geth的一个分支（这是使用最广泛的以太坊实现），并对其进行了修改，以将其转变为无需信任的第 2 层。这意味着在 Arbitrum 中运行的大部分代码与在以太坊中运行的代码相同。我们将这种尖端方法称为 Nitro（开发人员可以在此处查看代码库）

### Arbitrum 和 Optimism 有什么不同
Optimism 和 Arbitrum 是目前最大的两个以太坊 Layer-2 解决方案，都使用了 Optimistic Rollup 技术来拓展以太坊网络

尽管 Arbitrum 和 Optimism 都被称为 Optimistic Rollup，二者仍有一些本质上的区别。

其一，二者验证交易所使用的争端解决程序不同。Optimism 使用的是在 Layer-1 上执行的单轮欺诈证明，而 Arbitrum 使用链下执行的多轮欺诈证明。相比单轮欺诈证明，Arbitrum 的多轮欺诈证明更加便宜和高效，但是由于是链下执行，也会有一定的安全性风险

其次，虽然 Optimism 和 Arbitrum 都兼容 EVM，但 Optimism 使用的是以太坊的 EVM，而 Arbitrum 使用自己的 Arbitrum 虚拟机（AVM）。这导致 Optimism 只有 Solidity 编译器，而 Arbitrum 支持所有 EVM 编译语言（Vyper、Yul 等）

验证机制：Arbitrum 使用了一种名为”Fraud Proof”的验证机制来确保交易的安全性。在这个验证机制中，一些特殊的用户（称为验证人）会对提交的交易进行验证，并在需要时向以太坊主链提交证明，以保证交易的正确性。相比之下，Optimism 使用了一种名为”Fraud Prover”的验证机制。在这个验证机制中，一些特殊的用户（称为验证人）会在提交的交易被打包到区块之前，先验证其正确性，以避免在之后需要提交证明。
智能合约执行：Arbitrum 使用了一种名为”Arbitrum VM”的虚拟机来支持智能合约的执行。这个虚拟机与以太坊主链的虚拟机（EVM）相似，但是具有一些特殊的优化，可以实现更高的执行效率。Optimism 使用了一种名为”Optimistic Virtual Machine”（OVM）的虚拟机来支持智能合约的执行。OVM 与 EVM 兼容，但是可以通过一些优化来实现更高的执行效率。
治理模型：Arbitrum 和 Optimism 的治理模型也有所不同。在 Arbitrum 中，所有的验证人都可以参与投票，决定哪些交易可以被打包到区块中。在 Optimism 中，只有一部分特殊的用户（称为”sequencer”）可以打包交易到区块中，并决定区块的生成。 Arbitrum 和 Optimism 都使用了欺诈式证明（Fraud Proof）机制来确保交易的安全性。 欺诈式证明是一种可验证的证据，用于证明在区块链网络中发生了欺诈行为。在使用欺诈式证明的机制中，如果一个用户提交了一个不合法的交易或区块，其他用户可以使用欺诈式证明来证明这一不合法行为，并通过提交欺诈证明来获得相应的奖励。

### 生态方向
Arbitrum 更偏向于 DeFi 以及 GameFi 方向，Optimism 更偏向公共物品和基础建设，同时, Optimism 的未来版图是超级链网络，即打造一体化和互通化的 l2，而 arbitrum 更偏向于应用层面


### 欺诈证明
如果 arb 使用的是欺诈式证明，几天后发现是诈骗，假如资金已经被转出谁来赔偿这个损失？
在 Arbitrum 网络中，如果一个交易被验证人通过并打包进区块，而后被证明是欺诈行为，那么验证人将会失去相应的奖励，并需要支付一定的惩罚金。惩罚金将会被分发给提交欺诈证明的用户，作为他们的奖励。 但是，如果已经发生诈骗或其他不良事件，导致用户的资金被盗或损失，这并不属于 Arbitrum 网络本身的责任范畴。Arbitrum 网络提供的是一种安全性较高的交易验证机制，可以有效地减少欺诈行为的发生。但是，由于区块链技术的本质特点，一旦交易被确认，就无法被撤销或更改。因此，在进行交易时，用户需要自行承担风险，并确保自己的资产安全。




## 2024.12.11
