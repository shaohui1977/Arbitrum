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

# Helios

1. hi, 大家好。Arbitrum 最近不断的涌入资金，想来生态的发展正在日渐繁荣，刚好 LXDAO 开启了这场共学，那我一定要报名。欢迎和我组队，大家可以一起激发些 idea，看看能不能学完后开发个 demo，去参加黑客松。
2. 你认为你会完成本次残酷学习吗？ Maybe，哈哈哈哈哈 主要是我确实有点忙。 我尽量完成✅。 没有完成我也后面抽时间学完。

## Notes

<!-- Content_START -->

### 2024.12.10

1. 什么是 Arbitrum？
定义：Arbitrum 是一种专注于扩展以太坊的 Layer 2 解决方案，旨在提供更快、更便宜的交易处理，同时继承以太坊的安全性。
核心技术：
Arbitrum Rollup：一种 Optimistic Rollup 技术，利用欺诈证明（Fraud Proof）确保链上交易的正确性。

2. 为什么需要 Arbitrum？

以太坊的瓶颈：
* 每秒只能处理约 20-40 笔交易。
* 当网络拥堵时，Gas 费用会显著增加，导致交易成本高昂。

Arbitrum 的解决方案：
* 把大部分交易的计算和存储转移到 Layer 2（链下）处理，仅将结果提交到以太坊 Layer 1。
* 提供与以太坊主网相同的安全性，同时显著提高交易速度和降低费用。

3. Arbitrum 的工作原理

### Layer 2 和 Layer 1 的协作

Layer 2 处理：
* Arbitrum 在链下处理交易，并生成状态更新（如余额变化）。
* 将交易结果（如状态根或交易摘要）发送到以太坊 Layer 1。

Layer 1 验证：
* 以太坊“乐观地假设”所有 Layer 2 交易是正确的。
* 如果有问题（如恶意操作），任何验证者都可以提交“欺诈证明”，要求重新验证。

### 欺诈证明（Fraud Proof）机制

核心逻辑：
* 如果有人认为 Layer 2 的结果错误，可以提交欺诈证明。
* 验证者在以太坊上重新计算交易，判断提交结果的正确性。

结果：
如果发现错误：
提交错误数据的验证者会被经济惩罚（质押资金被扣除）。
恢复到正确的状态。
如果无误，挑战者会失去质押资金。

4. Arbitrum 的关键特点

安全性
* Arbitrum 继承了以太坊的安全性：
* 数据直接存储在以太坊上，任何人都可以验证交易是否正确。
* 只需一个诚实的验证者，就可以确保系统安全。

去信任化：
* 验证者的操作通过以太坊智能合约裁定，减少对中介的信任需求。

高效性

交易速度快：
* 链下计算减少了以太坊的负载，提升了吞吐量。
* 费用更低：
* 仅需支付链上存储结果的 Gas 费用，而非每笔交易的计算费用。

开放性
* 任何人都可以成为验证者：
* 无需许可，只需运行开源软件并质押 ETH 即可。
* 开发者友好：
* 支持以太坊智能合约的部署，无需修改现有代码。

 5. Arbitrum 的生态系统

开发者应用：
* 开发者可以在 Arbitrum 上部署与以太坊完全兼容的智能合约。
* 支持所有现有的以太坊工具（如 Remix、Truffle）。

用户体验：
* 用户可以通过钱包（如 MetaMask）直接与 Arbitrum 网络交互。

6. 总结：Arbitrum 的优势

安全性：数据存储在以太坊上，继承以太坊的强大安全性。

高效性：快速处理交易，降低 Gas 费用。

开发者友好：兼容以太坊工具链，无需额外学习成本。

灵活性：验证者开放，任何人都可以参与。

### 2024.12.11

### Rollup
说白了就是把交易的信息打包到 L2 执行，然后把证明存储到以太坊

### ZK Rollups
使用零知识证明来验证交易信息，（零知识证明是一种算法：比如你告诉我房间里有什么东西来证明，这个房子是你的，而不是拿出钥匙打开房门。）

### Optimistic Rollups
乐观假设 + 欺诈证明

Arbitrum 是一个基于 Optimistic Rollups 的 L2 扩展方案，但它在以下方面有所优化：
	•	更高效的欺诈证明机制：Arbitrum 将欺诈证明分解为多轮挑战，使得欺诈检测的成本更低。
	•	EVM 兼容性强：支持直接迁移以太坊智能合约。
	•	性能优化：相较于其他 Rollup 方案，Arbitrum 在处理复杂合约时更高效。

### ZK Rollups vs. Optimistic Rollups
<img width="380" alt="image" src="https://github.com/user-attachments/assets/87bc5dcd-2910-4e51-ad00-f1182869258c">

### 2024.12.12
挑战状态流程图：

<img width="837" alt="image" src="https://github.com/user-attachments/assets/04119a56-3176-4e47-af4a-6849fa5c8350" />

**1. 起点：Start**
挑战游戏从这里开始，当一个验证者对 Layer 2 的状态（通常是区块或执行结果）提出质疑时。
**2. 阶段一：Block Challenge（区块挑战）**
目标：验证某个区块的输入状态和输出状态之间的过渡是否正确。
过程：
* 验证者对区块状态提出争议，二分协议（bisectExecution）逐步将争议范围从整个区块缩小到具体的有问题区域。
* 当争议锁定到一个单独的区块时，状态会转移到 Execution Challenge（执行挑战）阶段。
**3. 阶段二：Execution Challenge（执行挑战）**
目标：验证具体的交易执行步骤是否正确。
过程：
* 争议范围进一步缩小到某一笔交易的执行步骤。
* 通过多轮二分协议（bisectExecution），争议最终聚焦到单步执行。
* 当争议范围缩小到一步执行时，当前响应者可以调用 oneStepProveExecution，提供具体证明来展示某一步执行的结果是否正确。
**4. Timeout（超时）**
意义：为每个阶段设置了时间限制，确保挑战不会无限期拖延：
如果一方未在规定时间内响应挑战，则该方被判负。
超时处理是系统避免死锁的重要机制。
**5. Emergency Upgrade（紧急升级）**
目的：如果挑战结果可能出错或存在争议，系统会进入“等待超时”的状态，为潜在的紧急合约升级预留时间。
应用场景：
在极端情况下（如合约代码错误），开发团队可以利用这段时间对合约进行修复或升级。
**6. 结束状态：End**
挑战完成后，系统进入最终状态：
胜方：获胜方的状态声明被接受，并可能获得作恶方的押金作为奖励。
败方：失败方丧失押金，并且之前提交的状态被撤销。

**重点解析关键路径**
* bisectExecution：表示二分协议的操作，用来逐步缩小争议范围。
* oneStepProveExecution：表示争议最终锁定到单步执行时的证明操作。
* timeout：超时机制确保挑战有明确的时间界限，防止无休止争议。


假设 Layer 2 系统包含以下全局状态：
1. 输入状态（全局状态 S0）：
* 区块 X-1 的全局状态根。
* 包括账户 A 的余额 100 和账户 B 的余额 50。
2. 输出状态（全局状态 S1）：
* 区块 X 的执行后状态根。
* 声明账户 A 的余额为 80，账户 B 的余额为 70。
3. 问题：
* 挑战者（验证者）检查区块 X 的交易，发现某笔交易未正确更新余额（比如账户 A 实际应该剩余 90，而不是 80）。
* 挑战者发起挑战，逐步缩小到区块 X 的具体交易段或交易步骤。
4. 结果：
* 如果挑战成功，全局状态 S1 被撤销，系统回滚到 S0，或者部分交易被重新验证。

### 2024.12.12
<!-- Content_END -->
