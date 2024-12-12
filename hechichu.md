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

### 2024.12.11
### Arbitrum 概述

Arbitrum 是一套以太坊扩容解决方案，旨在简化去中心化应用的构建和使用。其提供了多个协议、链、服务和 SDK，支持 Arbitrum 生态系统的运行。

#### Arbitrum 组件：
1. **Arbitrum Rollup**  
   - 用于扩展以太坊智能合约的协议。
   
2. **Arbitrum AnyTrust**  
   - 更进一步扩展以太坊智能合约的协议，采用轻度信任假设。
   
3. **Arbitrum Nitro**  
   - 实现 Rollup 和 AnyTrust 协议的节点软件。
   
4. **Arbitrum 节点**  
   - 运行 Nitro 软件的机器，用于服务或与 Arbitrum 链交互。
   
5. **Arbitrum One**  
   - 公共的 Rollup 链。
   
6. **Arbitrum Nova**  
   - 公共的 AnyTrust 链。
   
7. **Arbitrum 桥接**  
   - 支持在以太坊、Arbitrum 和部分 Orbit 链之间转移 ETH 和 ERC-20 代币。
   
8. **Arbitrum Orbit**  
   - 支持运行自定义的 Rollup 和 AnyTrust 链。
   
9. **Arbitrum Stylus**  
   - 支持用 Rust 或其他编译成 Wasm 的语言编写与 EVM 兼容的智能合约。

#### Arbitrum 面向用户：
- **Arbitrum 桥接**  
  - 用户可以通过 Arbitrum 桥接在以太坊、Arbitrum 和部分 Orbit 链之间转移 ETH 和 ERC-20 代币。
  
- **Arbitrum Portal**  
  - 提供一个 Arbitrum 上 DApp 的目录。

- **快速入门（桥接）**  
  - 为第一次使用桥接的用户提供逐步指导。

#### Arbitrum 面向开发者：
- **Arbitrum 简介**  
  - Arbitrum 扩容解决方案的技术介绍。

- **快速入门（Solidity）**  
  - 针对 Web2 开发者，帮助其将 Solidity 智能合约部署到 Arbitrum。

- **快速入门（Rust）**  
  - 针对 Web3 开发者，帮助其使用 Stylus 将 Rust 智能合约部署到 Arbitrum。

#### Arbitrum 面向节点运行者：
- **运行完整节点**  
  - 帮助节点运行者在不依赖第三方节点的情况下访问 Arbitrum 链。

- **配置数据可用性委员会**  
  - 面向数据可用性委员会成员和 Orbit 链运营者，帮助其运行数据可用性服务器。

#### Arbitrum 面向链运营者：
- **Orbit 简介**  
  - 为有意了解 Orbit 价值主张和使用场景的读者提供的内容。

- **Orbit 快速入门**  
  - 帮助链运营者使用 Arbitrum Orbit 部署其第一个 Arbitrum 链。

#### 技术原理：
- **Nitro 内部架构**  
  - 对 Nitro 架构的技术深入分析。

- **AnyTrust 协议内部**  
  - 对 AnyTrust 协议的技术深入分析。

- **Arbitrum 白皮书**  
  - 介绍 Nitro 的原始白皮书。

- **DAO 文档**  
  - 支持 Arbitrum DAO 成员的文档。

### 2024.12.12
### Rollup 中文总结

**1. 什么是 Rollup**

Rollup 的核心是“归纳整理”，目的是缓解以太坊网络拥堵、提高 TPS（每秒交易量）并降低 Gas 费用。它的工作原理是将以太坊上的计算任务转移到 Layer 2 层协议进行处理，将计算结果压缩后再返回以太坊主网。

Rollup 类比：  
就像节假日景区的排队问题，平日直接排队效率较低，但节假日通过可信赖的代表来集中处理问题，可显著提升效率。

主要作用：  
- 将大量交易签名压缩成一个“VIP”签名块。
- 提升以太坊网络的吞吐量与运行效率。
- 同时保留链上部分数据以保障安全性。

Rollup 的两种主要实现方式为 **ZK Rollups** 和 **Optimistic Rollups**，它们分别有不同的特点和应用场景。

---

**2. 什么是 ZK Rollups**

**ZK Rollups** 利用零知识证明技术（ZK-SNARK），通过 Layer 2 验证者进行交易真实性认证，并将结果压缩后返回以太坊。

ZK 的四大特点：
1. **Zero Knowledge**：无需查看完整交易数据即可验证交易。  
2. **Succinct**：认证过程简洁高效。  
3. **Non-Interactive**：验证无需交互。  
4. **Argument of Knowledge**：确保数据的真实性和正确性。  

**优点**：
- 验证速度快，可快速将 Layer 2 的资产转回 Layer 1。
- 适合支付、银行和交易所等快速结算业务。

**缺点**：
- 算法复杂，对开发者有较高的技术门槛。

---

**3. 什么是 Optimistic Rollups**

**Optimistic Rollups** 采取“乐观假设”的方式，默认所有交易都是可信的，并由验证者通过奖惩机制发现和处理异常。

工作原理：  
验证者需要质押代币作为保证金，若其他验证者发现问题，可通过欺诈证明对其进行罚款。

**优点**：
- 开发友好，适合迁移原本在 Layer 1 的 Dapp 项目。
- 具有智能合约功能，可通过相应的治理代币进行治理。

**缺点**：
- 从 Layer 2 提币到 Layer 1 速度较慢（通常需要 1 周以上）。  
- 存在验证者作恶的潜在风险。

---

**4. 什么是 Arbitrum**

Arbitrum 是基于 Optimistic Rollups 的 Layer 2 协议项目，目前 TVL（总锁仓价值）位居前列。与 Optimism 项目相比，Arbitrum 采用多轮欺诈证明，更加高效，并且具有自己的虚拟机，增强了与以太坊网络的兼容性。

---

**总结**：
- **Rollup**：通过将任务“外包”给 Layer 2，提升以太坊运行效率。
- **ZK Rollups**：基于零知识证明算法，适合支付类业务，验证速度快但算法复杂。
- **Optimistic Rollups**：通过默认信任和奖惩机制，适合 Dapp 和 DeFi 项目，提币速度较慢。
- **Optimism 和 Arbitrum**：两者都属于基于 Optimistic Rollups 的协议项目，适配不同场景需求。  
- **ZKSync**：基于 ZK Rollups 的典型项目之一。

ZK Rollups 未来潜力大，但目前 Optimistic Rollups 更适合 Dapp 生态发展。
<!-- Content_END -->
