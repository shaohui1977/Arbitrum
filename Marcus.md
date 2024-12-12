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



### 2024.12.10

<!-- Content_START -->

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




### 2024.12.11

### Arbitrum DAO
Arbitrum DAO 也是采取 Pos 治理，即你持有的 arb 越多，你的投票权越大，arb 更偏向于社区驱动的方式来治理，但内部有一个安全委员会，为了防止一些治理攻击的方式出现，安全委员会是一组实体，负责确保 DAO 及其链的安全性和完整性。根据《宪法》规定，委员会可以绕过缓慢的投票程序，在出现安全紧急情况时迅速采取行动。安全委员会成员由 DAO 通过半年选举产生，安全委员会有 12 名成员，如果发生紧急问题，他们可以采取紧急行动，9/12 的投票即可直接行动

### Arbitrum 如何投票的
Arbitrum 的投票模式其实和大部分 DAO 都差不多，显示温度检查，一般是在论坛发布提案，然后到 Tally 上发起正式提案，通过即代表提案开始执行
Arb 同样对提案进行了分级，
Arbitrum 改进提案 (AIP)是由 Arbitrum DAO 成员提交的提案，提议对 Arbitrum 生态系统进行更改。AIP 有两种类型：宪法和非宪法：

宪法 AIP 是指修改宪法或 AIP-1 的文本或程序、在任何链上安装或修改软件、或在任何链上采取任何需要“链所有者”许可的行动。
非宪法 AIP 是所有其他 AIP，例如那些请求资金/补助金或向社区提供一般指导或信息的 AIP。
简单来说，一些动到协议本身的提案，如通胀系数，协议的一些新增组件，那么都是宪法 AIP，需要通过链所有者许可，需要再进行一次评判，其他的申请 Grants 和社区指导的提案就不是宪法 AIP

整个 AIP 投票过程（包括所有七个阶段）从第一阶段的温度检查开始通常需要 37 天（宪法 AIP）或 27 天（非宪法 AIP）。此过程旨在进行彻底的考虑和投票，确保每个人都有公平的机会表达他们的意见和担忧。

### Arbitrum 是如何分配 Grants 给社区的
Arbitrum 的预算是根据 AIP 来分配的，包括基金会自己的预算也要通过 AIP 来提出，然后 Arb 的 Grants 发放更多像是 DAO 内的委员会形式，形成了如 LTIPP 的激励计划(4500W arb),GCP(游戏催化剂)等分类别的资助委员会，一般资助委员会由几人组成，然后定期审阅项目并批款，同时也有一些总结报告
如：https://forum.arbitrum.foundation/t/long-term-incentives-pilot-program/20223

### Arbitrum 和 Optimism 的治理不同
Arb 的治理模型为 DAO、委托和质押模式
Arbitrum 由Arbitrum DAO治理，该 DAO 由 $ARB 代币持有者组成，他们可以提议并投票决定网络技术变更。代币持有者可直接参与治理，也可委托代表。Arbitrum DAO 最近通过了一项提议，引入 $ARB 代币质押，将其从纯治理代币转变为双重功能代币。未来，Arbitrum 的治理将基于质押 ARB 代币（$stARB）。这一变化旨在增加 $ARB的价值和提高治理参与度。

Arbitrum 希望快速提高治理参与度，因为目前只有约 10% 的 $ARB 流通量用于治理。Arbitrum DAO 通过智能合约实现，负责管理内置的财库系统。它还设有安全委员会，可在紧急情况下升级协议。安全委员会是治理结构的关键部分，负责在这些关键情况下做出决策，成员由 Arbitrum DAO 选举产生。Arbitrum 的治理结构是偏向财阀制的，因为$ARB代币持有者是系统的主要决策者。

OP 的治理模型为二院制
乐观采用非财阀治理系统，防止被单一实体或小群体控制。这意味着代币持有者不是协议升级、资源分配和创新的唯一决策者。即使积累大量OP治理代币，也无法轻易控制网络价值，因为乐观采用了两院制支架，其公民屋与代币屋相互制衡。

乐观集体是一个实验性的治理团体，治理细化不断迭代，因为他们认为长期愿景有时可能与短期价值相互冲突。

代币由 OP 治理代币持有者组成，他们可以直接投票或将投票权委托给信任的代表。公民屋则由在乐观生态象征的个人组成，公民由灵魂绑定的 NFT 拯救公民屋实行一人一票制，推动了民主进程。

代币屋负责协议升级和激励投票，而公民屋主要管理复古资助（主要项目性公共项目资助），确保协议追求长期目标，防止被实体特定控制。两院相互制，可以衡一院的核心职责被另一院否决。


### Arb 和 OP 谁的治理模型更好
这个说不上谁好谁坏，我整体的感觉是 Arb 更偏社区化一些，表面上没有明显的精英领导（当然背后也肯定有 arb 基金会或者安全委员会去推动），OP 更多的是社区+精英化治理的方式，二院的对抗，token house 为下议院，citizen house 为上议院，两院之间相互制衡
但是我目前感觉 arb 的治理偏社区化可能会导致一些治理资金的浪费，比如 treasuryDAO 的游戏激励计划，把整个 arb 都带向了游戏化的路线，但是游戏这个赛道又没起来，而 OP 感觉背后有 OP 基金会和 Coinbase 的助推，看起来更正规和精英化一些，也更偏向以太坊的核心层的感觉，arb 对比下来更社区化，当然也更分散，同时有一个问题就是社区化引导可能带来试错成本比较高，从而导致资金的浪费

<!-- Content_END -->  
