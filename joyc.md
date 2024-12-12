---
timezone: Asia/Tokyo
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

# hython

1. Base Tokyo的web3从业者
2. 你认为你会完成本次残酷学习吗？可能会

## Notes

<!-- Content_START -->

### 2024.12.10
> [!NOTE]
> A gentle introduction to [Arbitrum](https://docs.arbitrum.io/welcome/arbitrum-gentle-introduction)
#### Arbitrum 简介  
- 一种扩展以太坊的技术套件，使交易更便宜、更快，同时保持以太坊级别的安全性。  
- 背景以太坊的局限性：每秒只能处理 20-40 笔交易，竞争导致费用上升。 

#### Arbitrum 的优化  
- Rollup 的工作原理  
  作为以太坊的子模块运行，遵循“无罪推定”，必要时回到 L1 解决争议，保持安全性。  
- 交易效率的提升  
  批量提交交易，数据压缩存储在 L1，显著降低费用。  

#### 安全与信任  
- 验证者的角色  
  提供状态声明、处理争议，任何人都可以运行验证者以确保系统无需信任。  
- 欺诈检测  
  通过缩小到单一计算步骤解决争议，确保诚实方获胜。  

#### 用户体验  
- 兼容性  
  支持现有以太坊工具，提供类似以太坊的使用体验，但成本更低、速度更快。  
- 快速提现  
  使用快速桥接应用可避免 1 周延迟。  

#### 技术扩展  
- Stylus 新功能  
  支持 Rust 和 C++ 等高性能智能合约语言，提供更大灵活性。  
- AnyTrust 链的优势 
  数据离链存储，费用更低，适用于高吞吐量但去中心化要求较低的场景。  

#### 多链选择  
- 现有链
  - *Arbitrum One*：Rollup 链，去中心化、安全性高。  
  - *Nova*：AnyTrust 链，费用低。  
- Orbit 链
  开发者可构建自定义 Arbitrum 链。  

#### 决策机制  
- Arbitrum One 和 Nova 的未来由治理系统决定。  

### 2024.12.11
> [!NOTE]
> 轻松理解Rollup，ZK Rollups与Optimistic，Arbitrum的[区别](https://cloud.tencent.com/developer/news/1003179)

#### Rollup 
  是一种交易整理方法，将交易任务外包至 Layer2 协议执行，从而提升以太坊网络的效率与 TPS。  

#### ZK Rollups 
- **特点**：
  1. 零知识证明：无需查看完整数据即可验证。
  2. 简洁算法：验证过程简练高效。
  3. 非交互性：验证者身份无需公开。
  4. 数据真实性保障：通过复杂算法确保验证结果可靠。  
- **优点**：  
  - 提币到 Layer1 快速，适合支付和快速结算场景。  
- **缺点**：  
  - 算法复杂，对开发者有一定技术门槛。  

#### Optimistic Rollups
- **特点**：  
  1. 默认信任所有交易有效，后续验证期间通过奖惩机制处理错误。  
  2. 支持智能合约和项目迁移，兼容性强。  
- **优点**：  
  - 开发 Dapp 方便，支持无缝迁移项目。  
- **缺点**：  
  - 提币速度慢（通常需一周），存在验证者作恶风险。

#### Optimism与Arbitrum对比 
- 共同点：基于 Optimistic Rollups 开发，专注提升以太坊扩容性能。  
- 区别：  
  - **Optimism**：一次欺诈验证，交易计算依赖 Layer1 执行。  
  - **Arbitrum**：多轮欺诈验证，交易执行在独立虚拟机中完成，更兼容 ETH 网络。

#### 其他Layer2方案  
- **Zksync**：基于 ZK Rollups 方法，专注快速支付场景。  
- **Plasma、Metis**：其他 Layer2 协议，探索不同扩容方式。  
- **Truebit**：结合博弈与 AI，提升以太坊计算效率。

#### 总结
- **Rollup** 是以太坊扩容的核心思路。  
- **ZK Rollups**：适合支付类业务，验证严谨但开发难度较高。  
- **Optimistic Rollups**：适合 Dapp 和 Defi，但提币速度较慢。  
- **Optimism 与 Arbitrum**：基于乐观归纳的 Layer2 代表项目，各有优势与特性。 

<!-- Content_END -->
