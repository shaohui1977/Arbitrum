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


# {hechichu}

1. 自我介绍
  第一次参加共学活动,大三理科学生

2. 你认为你会完成本次残酷学习吗？
  可以的

## Notes

<!-- Content_START -->

### 2024.12.10

Arbitrum 简介
什么是 Arbitrum？
Arbitrum 是一个为扩展以太坊而设计的技术套件，提供比以太坊更低成本、更快速度的交易环境，同时保留以太坊级别的安全性。其核心产品 Arbitrum Rollup 是一种乐观汇总（Optimistic Rollup）协议。
为什么需要 Arbitrum 来扩展以太坊？
以太坊虽然强大，但其每秒交易量（TPS）有限（约 20-40），当达到上限时，用户竞争会导致交易费用上升。这种限制是为了确保以太坊的去中心化性质，使节点运行成本相对可控。

Arbitrum 简介
什么是 Arbitrum？
Arbitrum 是一个为扩展以太坊而设计的技术套件，提供比以太坊更低成本、更快速度的交易环境，同时保留以太坊级别的安全性。其核心产品 Arbitrum Rollup 是一种乐观汇总（Optimistic Rollup）协议。

为什么需要 Arbitrum 来扩展以太坊？
以太坊虽然强大，但其每秒交易量（TPS）有限（约 20-40），当达到上限时，用户竞争会导致交易费用上升。这种限制是为了确保以太坊的去中心化性质，使节点运行成本相对可控。

Arbitrum Rollup 的工作原理
乐观执行：
Arbitrum Rollup 通过将链上的大部分计算和存储转移到链下，降低以太坊主链（L1）的负担。主链假设 Arbitrum 上的活动是合法的，只有在发现违规时才会通过争议解决机制回到 L1 证明欺诈。

数据透明性：
所有交易数据都会被发布到以太坊主链上，即使出现争议，也能通过这些数据验证欺诈行为，从而继承以太坊的安全性。

验证者机制：
验证者推动 Arbitrum 链的状态更新，并在发现欺诈时提出争议。只要有一个诚实的验证者，链的安全性就能得到保障。


用户体验与开发者优势
与以太坊兼容：
用户可以使用熟悉的以太坊钱包与 Arbitrum 交互，开发者也能使用现有的以太坊工具部署智能合约。

更高效的交易处理：
Arbitrum 通过批量提交交易和数据压缩等技术，大幅降低了交易成本。

扩展性：
除了 Rollup，Arbitrum 还提供 AnyTrust 链 和 Orbit 链：

AnyTrust 链适用于不需要完全去中心化的应用，提供更低成本。
Orbit 链允许开发者创建自己的链，进一步扩展应用场景。


Arbitrum 简介
什么是 Arbitrum？
Arbitrum 是一个为扩展以太坊而设计的技术套件，提供比以太坊更低成本、更快速度的交易环境，同时保留以太坊级别的安全性。其核心产品 Arbitrum Rollup 是一种乐观汇总（Optimistic Rollup）协议。

为什么需要 Arbitrum 来扩展以太坊？
以太坊虽然强大，但其每秒交易量（TPS）有限（约 20-40），当达到上限时，用户竞争会导致交易费用上升。这种限制是为了确保以太坊的去中心化性质，使节点运行成本相对可控。

Arbitrum Rollup 的工作原理
乐观执行：
Arbitrum Rollup 通过将链上的大部分计算和存储转移到链下，降低以太坊主链（L1）的负担。主链假设 Arbitrum 上的活动是合法的，只有在发现违规时才会通过争议解决机制回到 L1 证明欺诈。

数据透明性：
所有交易数据都会被发布到以太坊主链上，即使出现争议，也能通过这些数据验证欺诈行为，从而继承以太坊的安全性。

验证者机制：
验证者推动 Arbitrum 链的状态更新，并在发现欺诈时提出争议。只要有一个诚实的验证者，链的安全性就能得到保障。

用户体验与开发者优势
与以太坊兼容：
用户可以使用熟悉的以太坊钱包与 Arbitrum 交互，开发者也能使用现有的以太坊工具部署智能合约。

更高效的交易处理：
Arbitrum 通过批量提交交易和数据压缩等技术，大幅降低了交易成本。

扩展性：
除了 Rollup，Arbitrum 还提供 AnyTrust 链 和 Orbit 链：

AnyTrust 链适用于不需要完全去中心化的应用，提供更低成本。
Orbit 链允许开发者创建自己的链，进一步扩展应用场景。

当前的 Arbitrum 产品
Arbitrum One：一个 Rollup 链，强调去中心化和安全性。
Nova：一个 AnyTrust 链，适合需要高吞吐量、低费用的应用。
此外，开发者可以基于 Arbitrum 的技术栈（如 Nitro 和 Stylus）创建高性能的智能合约，甚至使用如 Rust、C++ 等编程语言。

### 2024.12.10

<!-- Content_END -->
