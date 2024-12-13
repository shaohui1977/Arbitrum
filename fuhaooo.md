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

# Alfred

之前在Web2从事Java开发工作，接触Web3后在积极参与相关社区活动，不断学习中。希望能够在残酷学习中坚持下来，顺利完成。

## Notes

<!-- Content_START -->

### 2024.12.10

### 1. Arbitrum 的使命

Arbitrum 的使命是通过提供更高效、低成本和用户友好的解决方案，增强以太坊生态系统的可扩展性和可用性。它致力于构建一个去中心化、高性能的 Layer 2 扩展平台，使开发者和用户能够享受更快、更便宜的交易，同时保持以太坊的安全性和去中心化特点。

### 2. Arbitrum 的特点

- 高扩展性
：Arbitrum 是以太坊的 Layer 2 扩展方案，可以显著提高交易处理能力，降低拥堵和交易费用。
- 与以太坊的兼容性
：完全兼容以太坊的 EVM（以太坊虚拟机），开发者可以无缝迁移现有智能合约和 DApp。
- 低成本
：利用 Rollup 技术，大幅降低了链上计算和存储成本，使得小额交易也具有经济性。
- 安全性
：继承以太坊主链的安全性，所有交易在 Layer 1 上的验证确保了去中心化和抗审查性。
- 灵活性
：支持多种开发工具和语言，例如 Solidity，同时为开发者提供良好的文档和社区支持。

### 2024.12.11

### 3. Arbitrum 的原理

Arbitrum 采用了 Optimistic Rollup 技术，通过将大量交易打包（Rollup）并发送到以太坊主链上记录和验证，实现扩展和成本降低。

#### 交易流程

- 用户提交交易：用户的交易首先被发送到 Arbitrum 的 Layer 2 网络。
- 批量打包：多个交易被打包成一个批次，并生成一个状态更新。
- 状态提交：批量交易的摘要（状态根）被提交到以太坊主链。
- 欺诈证明：如果有恶意操作，验证者可以提交欺诈证明，以挑战提交的状态并恢复正确性。

#### 核心技术

- Rollup 技术：将计算和存储移到链下，仅将交易摘要记录到主链。
- 欺诈证明机制：通过挑战者模型确保系统的正确性和抗审查性。
- 以太坊安全性继承：利用 Layer 1 的共识机制，保证 Arbitrum 的交易数据和状态更新的最终性。
### 2024.12.12

### 4. Rollup 概念概述
Rollup 是一种二层扩展解决方案，旨在提高区块链的可扩展性和性能，特别是在以太坊等区块链上。通过将大量交易和计算工作“卷起”并批量处理，这些交易的执行和数据存储仍然依赖于主链（如以太坊），但通过将交易的计算和存储从主链转移到二层，显著提高了交易吞吐量和降低了费用。

原理：
- 成本优化：将⼤部分运算与存储任务移交至L1链下也即L2上。
- 安全保障：L2上的交易内容与交易后的状态，会同步⾄以太坊L1，通过合约来校验 状态转换的有效性。

Rollup 的核心概念是将交易数据打包到主链之外进行处理，但通过机制保证数据的完整性和安全性。这使得它可以提供和主链一样高的安全性，同时大幅提高处理速度和降低成本。常见的 Rollup 类型包括 Optimistic Rollups 和 ZK-Rollups

防止Rollup排序器作恶的状态校验⽅式，分为欺诈证明（Fraud Proof）和有效性证明（Validity Proof）两类。使⽤欺诈证明的Rollup⽅案称为OP Rollup（Optimistic Rollup，OPR），⽽因为一些历史包袱，使⽤有效性证明的Rollup往往被称为ZK Rollup（Zero-knowledge Proof Rollup，ZKR)，而不是Validity Rollup。

### 5. Fraud Proofs 欺诈证明机制
欺诈证明机制 是在 Optimistic Rollups 中用来确保二层链正确性的机制之一。在这种模型下，交易的执行被假定是有效的，直到有人提出异议（即“挑战”）。这种机制可以通过以下步骤工作：

- 交易提交：用户在二层 Rollup 上发起交易，交易数据和状态变更会被“卷起”并提交到以太坊主链。主链会记录这些批量交易的哈希值。

- 乐观执行：在 Optimistic Rollup 中，假设这些交易是有效的，并且会在链上验证这些交易。理论上，交易会立即被认为是有效的，不需要立即进行复杂的计算。

- 欺诈挑战期：将状态提交到 Rollups 合约后，有一个时间窗口允许其他参与者查看这些交易。如果某个参与者认为 Rollup 上的某个交易是不合法的或恶意的，他们可以提出一个 欺诈证明，即对该交易的合法性进行挑战。

- 欺诈证明的验证：当有人提出欺诈证明时，网络会进行审查，验证该交易是否真正无效。如果证明成功，恶意或无效的交易会被回滚，相关提交的交易也会被撤销。

- 奖励和惩罚：提出有效欺诈证明的挑战者会获得奖励，而那些提交无效交易的节点（比如欺诈者）则会受到惩罚。惩罚通常是扣除抵押金，或者其他形式的经济惩罚。

### 2024.12.13
### 6. Zero-Knowledge Proof 零知识证明机制
零知识证明（简称 ZKP）是一种密码学方法，允许一方（证明者）向另一方（验证者）证明某个声明是真实的，而无需透露任何与该声明相关的具体信息。自20世纪80年代首次提出以来，零知识证明在隐私保护、身份验证、区块链技术等多个领域得到了广泛应用和深入研究。

零知识证明是一种协议，满足以下三个核心属性：
- 完备性（Completeness）：如果声明为真，诚实的验证者将在协议结束时被说服。
- 可靠性（Soundness）：如果声明为假，恶意的证明者无法说服诚实的验证者，除非以极低的概率。
- 零知识性（Zero-Knowledge）：如果声明为真，验证者不会学到任何除了声明为真之外的其他信息。

### 7、Rollup 协议
欺诈证明虽然不能像零知识证明那样具有⾼度的简洁性，但Arbitrum使⽤了⼀种“多轮分割-单步证明”的轮流式交互流程，最终需要证明的仅仅是单⼀的虚拟机操作码，成本相对较⼩。

Rollup协议的核心合约是RollupProxy.sol，在保证数据结构一致的情况下，使用了一个罕见的双重代理结构，一个代理对应两个实现RollupUserLogic.sol和RollupAdminLogic.sol，在Scan等工具中目前还无法很好的解析。

另外还有ChallengeManager.sol合约负责管理挑战，OneStepProver系列合约来判定欺诈证明。
![image](https://github.com/user-attachments/assets/a021e2c0-a0df-4125-912c-0fc22d246028)

ChallengeManager合约负责验证对挑战步骤的细分过程：

1.细分是一个双方轮流互动的过程，一方对某个Rollup Block中包含的历史数据进行分段，另一方指出是哪部分数据片段有问题。类似于二分法（实际是N/K）不断渐进缩小范围的一个过程。

2.之后，可以继续定位至哪条交易及结果有问题，再进一步细分至该交易中有争议的某条机器指令。

3.ChallengeManager合约只检查对原始数据进行细分后，产生的『数据片段』是否有效。

4.当挑战者和被挑战者定位到了将被挑战的那条机器指令后，挑战者调用oneStepProveExecution()，发送单步欺诈证明，证明这条机器指令的执行结果有问题。

### 8、单步证明
单步证明是整个Arbitrum的欺诈证明的核心。WAVM，Wasm Arbitrum Virtual Machine，它是一个由ArbOS模块和Geth（以太坊客户端）核心模块共同编译成的虚拟机。由于L2与L1有许多截然不同的地方，原始的Geth核心必须经过轻量修改，并且配合ArbOS一起工作。所以，L2上的状态转换其实是ArbOS+Geth Core的共同手笔。
![image](https://github.com/user-attachments/assets/095379f9-7565-4401-bf78-0be0a7d38d71)

Arbitrum的节点客户端（排序器、验证者、全节点等），是将上述ArbOS+Geth Core处理的程序，编译为节点主机能直接处理的原生机器代码（for x86/ARM/PC/Mac/etc.）。

如果把编译后得到的目标语言更改为Wasm，就得到了验证者生成欺诈证明时使用的WAVM，而验证单步证明的合约上，模拟的也是WAVM虚拟机的功能。

那为什么在生成欺诈证明时，要编译为Wasm字节码？主要还是因为，验证单步欺诈证明的合约，要用以太坊智能合约模拟出 能处理某套指令集的虚拟机VM，而WASM易于在合约上实现模拟。
![image](https://github.com/user-attachments/assets/149c286b-e139-46e5-b715-9c81820c68a7)

但WASM相比于Native机器代码，运行速度略慢，所以只有在欺诈证明生成及验证的时候，Arbitrum的节点/合约才会用到WAVM。

在之前的多轮互动细分后，单步证明最终证明的是WAVM指令集中的单步指令。
<!-- Content_END -->
