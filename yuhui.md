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

# {yuhui}

1. 自我介绍 yuhui
2. 你认为你会完成本次残酷学习吗？ yes

## Notes

<!-- Content_START -->

### 2024.12.10

笔记内容：Arbitrum是一种基于以太坊的Layer2扩容方案，旨在提升以太坊的可扩展性和交易效率，同时保持去中心化和安全性，在仔细阅读白皮书后我总结出Arbitrum的使命有以下三点：1.提升以太坊网络的扩展性 通过减少主网的交易负载，降低交易费用，提高交易吞吐量 2.保持以太坊的安全性和去中心化 利用以太坊主网作为最终的安全层，确保扩展解决方案不会牺牲以太坊的核心价值。 3.增强用户体验 提供快速、低成本的交易，支持智能合约的无缝迁移，让开发者和用户更容易采用 Arbitrum的特点有以下三点：1.具有高效性 低成本：通过批量处理交易（Rollup），显著降低交易费用。 高吞吐量：相比以太坊主网，Arbitrum可以处理更多的交易，减少拥堵。2.具有兼容性 以太坊兼容性：支持现有的以太坊智能合约和开发工具，开发者可以直接将智能合约迁移到Arbitrum。无需更改代码：支持Solidity和其他以太坊虚拟机（EVM）兼容的语言。Arbitrum的基本原理Arbitrum的工作机制基于一种称为 Optimistic Rollup 的技术。以下是其关键原理：1.批量处理交易在Arbitrum链上，交易被打包处理后，通过Rollup技术将其结果提交到以太坊主网。交易数据会以压缩形式存储在以太坊上，从而减轻主网的存储和处理压力。2.欺诈证明（Fraud Proofs）Arbitrum默认所有提交的数据都是有效的（Optimistic假设）。如果有验证者质疑某笔交易的有效性，可以提交欺诈证明，启动争议解决过程。一旦欺诈行为被确认，相关交易会被回滚，并惩罚恶意验证者。3.链下计算，链上验证大部分交易计算在Arbitrum链下完成，以节省资源和时间。交易结果通过加密证明提交到以太坊主网，确保最终状态的一致性。4.状态通道和侧链结合Arbitrum结合了状态通道和侧链的优点，既提供快速响应，又确保安全性和去中心化。总结而言，Arbitrum通过技术创新和对以太坊生态的深度支持，为解决区块链的三难问题（安全性、去中心化、可扩展性）提供了一个平衡且高效的解决方案。
### 2024.12.10

<!-- Content_END -->
