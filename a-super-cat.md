---
timezone: Asia/Shanghai
---

> 请在上边的 timezone 添加你的当地时区，这会有助于你的打卡状态的自动化更新，如果没有添加，默认为北京时间 UTC+8 时区
> 时区请参考以下列表，请移除 # 以后的内容

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

---

# 志伟

1. 大家好，社区新人一枚，很高兴与大家一起学习，有一种大家大学期末考试前一起交流学习的感觉哈哈哈
2. 会完成的，闹钟已调好

## Notes

<!-- Content_START -->

### 2024.12.10

#### 为什么需要Arbitrum？

答：以太坊区块链大概每妙可以完成20到40个交易（以太坊所有的用户形成的交易次数）；当交易达到上限时剩下的用户就需要去竞争以使他们的交易被链打包进去，竞争也使打包的费用升高了（在区块链中，为交易支付的打包费用越高，则越可能会被“矿工”优先打包。）

​	Arbitrum采用乐观Rollup策略，将大部分运算与存储任务移交至L1链下（即L2上）来优化成本。L2大多是运行在单台服务器，也就是排序器（Sequencer/Operator）上的一条链。这种方式在“区块链不可能三角”中舍弃了“去中心化”来换取TPS与成本上的优势，允许L2代替以太坊处理交易指令，从而降低成本（虽然排序器作为系统中枢带有中⼼化色彩，但在成熟度比较高的Rollup方案中，中心化排序器仅能实施交易审查等软性作恶⾏为，或者恶意宕机，但在理想状态的Rollup⽅案中，有相应的⼿段进⾏遏制（比如强制提款或排序证明等抗审查机制））。

#### Arbitrum的原理

答：Arbitrum采用乐观Rollup，这意味着暗含一条信任假设：任意时刻⾄少有⼀个诚实的L2验证者节点。不主动验证提交过来的数据，乐观地认为这些数据没有问题。如果提交的数据有错误，L2的验证者节点会主动发起挑战。挑战过程可概括为可以概括为多轮互动式细分、单步证明。在细分环节，挑战双⽅先对有问题的交易数据进⾏多轮回合制细分，直⾄分解出有问题的那⼀步操作码指令，并进⾏验证。因没有通过验证的L2 Block不具备最终确定性，故验证不通过时排序器可以对这些Block进行回滚。一般而言被提交到Layer1上的L2数据无法回滚，可以具有最终确定性。


### 2024.12.11

#### Layer2有哪些技术类型？

1. Channels通道（状态通道、支付通道）：这种方式概括起来为：在通道建立的时候要锁定一些资金，这个存款也作为虚拟的“押金”，这个通道允许交易双方在链下进行多次交易，当通道不再需要时，双方确认最终状态，并生成最终状态的签名。然后这个最终状态提交到区块链，区块链会进行签名验证和结算，正式关闭通道。

2. Sidechains 侧链：侧链使用自己的[共识机制](https://www.horizen.io/academy/consensus-mechanisms/)进行操作，是一条独立运行但可以跟主链互通的区块链。它提供了一条快速通道，于特定时候可以让资产可以在主链和侧链之间快速流通。但由于侧链是独立运行的，不受主链保护，所以它自己要负责维护安全。这需要消耗额外的算力或资源，例如 POS 或 POW 共识机制。目前以太坊比较知名的侧链解决方案主要为 xDai 和 Gnosis 链。这些侧链都为以太坊提供了高速通道。开发者可以利用这些侧链的免费节点来开发 dApp。

   虽然侧链不需要向主链提交状态数据，但许多侧链仍然选择这样做，以利用更大、更去中心化的链的安全性。

3. Validiums：Validiums 与侧链类似，是一条独立运行的区块链，但与主链紧密连结，Validiums 使用的主要是零知识证明而不是传统的工作量证明或权益机制证明。但与zk-Rollup不同交易数据不存储在 Layer1 主链上，所以 Validium 可以在不暴露真实交易讯息的情况下，证明交易是有效且符合预设规则的。但是跟侧链一样，Validium 也有局限性。因为不依赖主链安全，需要自建共识层，对开发者的要求较高。智能合约支持也相对有限。简单来说，Validium 是介于侧链和 Layer2 Rollup 之间的技术。它与主链有连接桥梁，可以交互资产。但需要自行确保安全性。

4. Rollups：Rollup 是现今最热门的 Layer2 技术，基本概念是把交易资料打包后以 Rollup （打包整理）的形式提交到 Layer1，主要分为两种流派。

   * Optimistic Rollup:Optimistic Rollup 是目前使用最广泛的 Layer2 解决方案，代表项目有 Arbitrum、Optimism 等。优点是易于开发和部署，可以快速吸引应用，缺点是有一定欺诈风险，需要依赖经济机制防止。
   * zk-Rollup:zk-Rollup 使用称为零知识证明（ZK-proofs）来验证交易的真实性，这可用于改善区块链上的隐私，因为它允许在不泄露有关交易的敏感讯息的情况下，来进行验证交易，缺点是较不易开发，代表项目有 zkSync、Polygon zkEVM、Linea。零知识证明技术的出现，将有可能会成为企业未来的采用方案，因为它可以仅向第三方（用户）显示他们想要传达的讯息，同时安全地传输敏感数据。

   * 总结：整体来说，ZK rollups 可以带来更高的效率，但 Optimistic Rollup 和 ZK Rollup 之间最大的区别在于 Optimistic 可以与 EVM 直接兼容，因此 Layer1 上的任何可能在 Layer2 上都是可直接实现的。但是，为了解决 ZK rollups 的 EVM 兼容问题，后续也逐渐出现了 zkEVM 解决方案（例如：**[zkSync](https://zksync.io/)**、[Polygon zkEVM](https://polygon.technology/polygon-zkevm?fbclid=IwAR2U3DocnBaFDwFLjwSKuDGk4e7yRhH6M6OfgA8i2s6xFeF2j7KqDbzh6q4)、**[Scroll](https://scroll.io/)**）

#### 欺诈证明过程

Arbitrum 的方法基于对争议的剖析。如果 Alice 的断言涉及了 N 个执行步骤，那就让她曝光出两个各涉及 N/2 个步骤的断言，然后让 Bob 选择一个来挑战。这样一来，争议的规模就缩小了一半。这个过程持续进行，每一回合都将争议的规模缩小一半，直到争议的范围变成一个执行步骤。注意，直到此时为止，L1 引导合约都不必考虑实际上执行了什么。仅当争议被缩小到单个执行步骤时，L1 引导合约才需要理解这一步要执行什么指令，以及 Alice 对该步的断言是否为真，以此解决争议。

交互式证明背后的关键原理是，如果 Alice 和 Bob 有所争议，Alice 和 Bob 应尽可能做链下的工作来解决争议，而不是让 L1 合约承担负担。

### 2024.12.12

#### Arbitrum One

Arbitrum One是Arbitrum的旗舰链，建立在Optimistic Rollup技术之上。Arbitrum的架构有部分在L1上有部分在L2上，EthBridge 负责对 Arbitrum Rollup 协议进行仲裁，以及维护 Arbitrum rollup 在以太坊链上的收件箱和发件箱。Arbitrum 虚拟机（AVM）是 EthBridge 提供的功能，是 L1 和 L2 之间的网关。AVM 能够读取输入，并基于这些输入执行计算，从而产生输出。ArbOS 运行在 AVM 上，确保智能合约在 Arbitrum 链上执行。ArbOS 完全存在于 L2 上，并像在以太坊上一样运行 EVM 合约。

#### Nitro

Nitro是One的升级。升级版的Nitro费用更低，以太坊兼容性更好以及zk证明更加简洁。支持Nitro的关键创新可概括为四点：证明程序、以Geth为核心、实现执行与证明分开、交互式欺诈证明的Optimistic Rollup。

Arbitrum 的旧方案方案是通过定制的 Arbitrum 虚拟机（AVM）来模拟 EVM，它的一些内部逻辑在EVM 不一致（例如Gas的计算），所以仅限于低级指令。而Geth则基本完全支持以太坊的数据结构、格式和虚拟机，所以可以实现以太坊高度兼容。其关于欺诈证明的代码会编译为wasm格式，可移植、体积小、加载快、并且兼容web。而且Nitro又对wasm格式进行了微调，让它更适合与链交互。

在WASM代码上进行Arbitrum的交互式欺诈证明，就取代了Arbitrum虚拟机（AVM）的架构，直接以标准的语言和工具来构建和编译。

#### Nova

Arbitrum Nova 是基于 AnyTrust 技术搭建的新链，专为游戏、社交应用程序和对成本更敏感的用例而设计。Nova 提供了 2 种数据发布方式，一种是像 Nitro 一样以 Calldata 的形式发布完整数据，另一种是发布 DACert 证明数据的可用性。

Nova 的定序器将完整的数据集同时发送给所有 DAC 委员会的成员，委员会签名后把带有签名的证明返回给定序器，定序器收集到足够多的证明就能将它们聚合并创建有效的数据可用性证明（DACert），然后把 DACert 发布到主网。如果定序器没有收集到足够多的证明，Nova 会回退到 Rollup 模式（以 Calldata 形式发布数据到主网）。

相对于 One 而言，Nova 通过牺牲一定的安全性来提高性能，游戏社交类等需要高频交互的 Dapp 适合部署在 Nova 上。


<!-- Content_END -->
