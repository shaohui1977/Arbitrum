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


# {猪大虫}

1. 自我介绍
  第一次参加共学活动

2. 你认为你会完成本次残酷学习吗？
  可以的

## Notes

<!-- Content_START -->

### 2024.12.10

笔记内容
什么是 Arbitrum？

Arbitrum是一个生态系统，涵盖了多个基于以太坊的 Layer 2 解决方案，Arbitrum Rollup是Arbitrum的核心产品，是Optimistic Rollup 技术的一种具体实现。

什么是Optimistic Rollup？

Optimistic Rollup 是一种 Layer 2 扩展技术的协议和机制，主要特点是：
假设机制：默认认为提交的交易和状态是正确的（Optimistic）。
欺诈证明：允许用户通过欺诈证明（Fraud Proof）挑战提交的错误交易或状态。
设计目标：减少主链上的计算和存储负担，同时保持高性能和低成本。
所以Optimistic Rollup 是一个技术框架。

Arbitrum Rollup相比于原生的Optimistic Rollup做出了什么优化？

更短的挑战期：Arbitrum Rollup使用了增强的挑战期，允许挑战者使用简化的证据提交，从而加快挑战的响应速度，并且只针对有争议部分进行挑战，不需要完全重新计算整个交易。
更低的复杂度与更高的效率：Arbitrum Rollup只对争议部分进行验证，使用n/2的方式缩小每一步的范围，直到欺诈证明的某一具体步骤，降低了挑战成本与时间。
回滚与确认速度：更快，快速回滚错误状态
经济激励：更明确和灵活的经济激励与惩罚机制

### 2024.12.10

<!-- Content_END -->
