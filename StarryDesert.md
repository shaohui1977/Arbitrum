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

# {StarryDesert}

1. 自我介绍

   2024年应届生，干过java，新入行web3小白，参加过sui的黑客松并获奖(虽然只是入围奖)。

2. 你认为你会完成本次残酷学习吗？

   我觉得我会

## Notes

<!-- Content_START -->

### 2024.12.10

笔记内容

#### 初识 Arbitrum

Arbitrum是一种基于以太坊（Ethereum）的Layer 2扩容解决方案，旨在提高以太坊网络的交易处理能力和降低交易成本。

##### 使命

1. 保证以太坊的安全性和去中心化，利用主网作为最终的安全层。
2. 提升用户的体验，开发者无需更多的学习成本，便能轻松且快速的部署和迁移合约。
3. 减少主网的负载，做到了降低交易费用和提高交易速度。

#### 核心机制：Optimistic Rollup

1. **批量处理**：将多个交易合并成一个单一的交易，让多个交易被打包压缩以压缩数据的方式存储在主网上，这样可以有效的减少主网的交易负载，降低交易费用
2. **欺诈证明**：乐观的假设链上的Arbitrum 上的活动均为合法的，如果有验证者质疑某比交易的合法性，可以提交声明，启动挑战。一但该比交易的欺诈行为被确认，则此交易会被回滚，并惩罚恶意的验证者
3. **使用Off-chain的链下计算**：Arbitrum上交易的计算都在链下进行，然后将计算的结果提交到以太坊主网。通过这种方法提高了交易的处理能力并降低了交易成本

#### 今日总结

通过今天的学习，我对Arbitrum和其核心机制的Optimistic Rollup有了初步的了解，认识到其在以太坊扩容解决方案中的重要性和潜力。

### 2024.12.11

笔记内容

#### Rollup, ZK Rollups与Optimistic，Arbitrum的区别

1. **Rollup**：是一种整理方法，将一堆交易任务送到Layer2协议去处理，从而提升以太坊的运行效率。
2. **ZK Rollups**：是一种利用零知识证明的密码学算法，在无需知道验证者是谁的情况下，完成外包工作的Layer2方法。适合Payment等需要快速交易的业务，但算法稍复杂。
3. **Optimistic Rollups**：是一种利用一堆验证者，在默认所有打包均为合法的情况下，通过奖惩机制，监督发掘是否有Bug的Layer2方法。
4. **Optimistic，Arbitrum**：两者都是以**Optimistic Rollups**协议为基础开发的项目，但具体有以下不同：
   - **验证机制**：**Optimistic** 只进行一轮欺诈证明，而**Arbitrum**进行多轮欺诈证明。
   - **交易执行**：**Optimism**的交易计算依靠Layer 1来执行，而**Arbitrum**的交易则在其自己的虚拟机中执行，无需依赖Layer 1。
   - **虚拟机**：**Arbitrum**有自己的虚拟机，更加兼容ETH网络，而**Optimism**则依赖Layer 1的虚拟机。

### 2024.12.12

笔记内容

#### Arbitrum的仲裁机制

- 当验证者对某比交易发起挑战时，**挑战管理器**（**ChallengeManager**）将仲裁挑战游戏，通过对全局状态（包括块哈希）进行二分来缩小挑战范围，直到挑战仅剩下一个块。

- 挑战状态机有三个阶段：**Block challenge**、**Execution challenge**和**oneStepProveExecution**。
  - **Block challenge**：挑战首先将全局状态（包括区块哈希）一分为二。在对实际的机器执行提出争议之前，争议将缩小到单个区块。一旦挑战被一分为二到单个区块，当前响应者就可以调用 `challengeExecution`。
  - **Execution challenge**：一旦缩小到单个区块，就可以将实际的机器执行一分为二。一旦执行被平分为单个步骤，当前响应方就可以调用`oneStepProveExecution`。
  - **oneStepProveExecution**：当前响应方必须提供校样数据才能执行计算机的某个步骤。如果执行该步骤以与之前断言不同的状态结束，则当前响应方将赢得质询。

- **General bisection protocol**：涉及对任何程度的分割，当前回应者必须选择相邻的两个段来挑战，并提供一个起始段等于第一个段但结束段不同于第二段的二分。

  - 挑战的程度是指段哈希的数量减一，一个段和下一个段之间的距离根据程度和段长度计算。
  - 挑战的进展是通过确保每个二分都具有至少 `min(40, numStepsInChallengedSegment)` 的度数，以确保挑战取得进展。

  - 赢得挑战使当前回应者成为赢家的对手，设置状态哈希为 0，从而结束游戏。

#### 交互式欺诈证明的特点

1. **高效性**：交互式证明可以解决大于一笔交易的争议，减少了对L1区块的空间占用，降低了rollup成本。
2. **灵活性**：交互式证明允许实现上的更大灵活性，例如加入EVM中还不存在的指令。
3. **无合约大小限制**：交互式证明无需为每一个L2合约创建一个以太坊合约，所以也不要求合约符合以太坊合约的限制。
4. **低复杂度**：交互式证明只需检查**"Alice"**和**"Bob"**的操作**在往正确的方向走**，而不需要模拟一整笔交易的执行。
5. **高交易级gas limit**：交互式证明可以处理大gas容量的Arbitrum交易，即使一笔交易gas消耗量太大，也仍有可能可以放进Arbitrum的区块内。

   这些特点使得交互式证明成为**Arbitrum**的核心设计，并使得**Arbitrum**能够高效、灵活地解决争议和执行交易。

### 2024.12.13

<!-- Content_END -->
