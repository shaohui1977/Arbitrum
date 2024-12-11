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

# Tomas

1. Hi，大家好，我是一个社区新人，之前一直在关注共学这一种形式，这次鼓起勇气参与这次社区共学活动，希望可以通过学习提升自己。
2. 你认为你会完成本次残酷学习吗？我已经做好完成的准备。

## Notes

<!-- Content_START -->

### 2024.12.10
# Arbitrum

> Arbitrum网络是Ethereum网络的扩展网络，它设计出来的目的就是为了扩展Ethereum并解决Ethereum网络中的一些问题。在Arbitrum网络中你可以做一切你可以在Ethereum网络中做的事情，使用web3App，部署智能合约。但是，使用Arbitrum 你的交易的手续费会更低，你交易所花费的时间会更少。其依靠的核心的核心机制是Optimistic Rollup protocols（乐观假设）其将大部分交易移到链下执行，降低交易成本提高吞吐量。同时其安全性依靠Ethereum主网，保证了安全性。
> 

**The Arbitrum Rollup mechanism adopts an “innocent until proven guilty” attitude.**

***Arbitrum的核心机制为 Arbitrum Rollup*** 

# Some introduction about Arbitrum

> [https://docs.arbitrum.io/welcome/arbitrum-gentle-introduction](https://docs.arbitrum.io/welcome/arbitrum-gentle-introduction)
> 

## Why do we need Arbitrum?

因为以太坊的TPS（transactions per second）太低，大概只有20到40，达到上限后用户进行竞争导致交易fee上涨，而设计导致其瓶颈已经很难提升。

## Why does Ethereum have a low TPS?

因为以太坊就是设计决定，必须要在所有节点上同步交易，并确保其可行性（分布式账本），其势必会影响j交易的并发性和交易速度。

## How does Arbitrum solve the problem?

Arbitrum 通过引入Layer 2 网络和 Arbitrum RollUp 来解决这个问题，Arbitrum Rollup 是作为Ethereum 子模块运行的，与传统意义上的L1交易不同，我们不需要在Ethereum节点上处理每一笔Arbitrum交易，相反，Ethereum采用了一种：**“innocent until proven guilty”  在证明其有罪前其即是无罪的理论。当违规操作出现时，争议处可以被反驳，如果反驳成功无效的交易被忽视，欺诈者会被采取经济惩罚；**

这种引入链下的操作极大的增加了TPS，提高交易速度，减少交易过程中产生的 gas fee。

## Who does this work to prove fraud?

> 把Arbitrum chain状态推向L1，并且对其他有可能不正确的声明提出质疑的叫做 **vaildator**
> 

**vaildator** 并没有权限限制，只要可以运行节点，并且愿意质押一定数量的Ether，都可以成为 **vaildator 。此外只要有一个诚实的节点那么就可以确保这条链是安全的。因为一个vaildator可以抓到任意数量的欺诈者，这也大大增强了其中的安全性。**

# How exactly is Fraud Proven? (欺诈行为是如何被证明的)

当两个validator 产生了不同的判断，最多只有一个 validator 是诚实的。在冲突发生的情况下，他们会进行一个交互游戏 **ChallengeManager** 这个游戏会逐渐缩小冲突范围，直到缩小到一个简单的计算，例如两数相加。这是在L1中进行的，并且会证明其中有一方说的是真话。

### 2024.12.10

<!-- Content_END -->

<!-- Content_START -->

### 2024.12.11

今天按照https://docs.arbitrum.io/build-decentralized-apps/quickstart-solidity-hardhat上的方法搭建了，Dapp并使用本地节点进行了部署。

# RollUp的作用

Roll up 译为压缩整理，Roll up 的作用就是将区块链上需要计算的内容Copy到以太坊之外的Layer2协议进行计算。然后再将结果结果信息打包发送到链上网络。
ZK RollUp 引入了零知识证明，通过复杂严谨的逻辑验证方法进行验证。来认证不同数据的真实性，验证完成后将存有大量签名的数据存入区块链网络。

### 2024.12.11

<!-- Content_END -->
