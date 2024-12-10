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

# 志伟

1. 大家好，社区新人一枚，很高兴与大家一起学习，有一种大家大学期末考试前一起交流学习的感觉哈哈哈
2. 会完成的，闹钟已调好

## Notes

<!-- Content_START -->

### 2024.12.10

#### 为什么需要Arbitrum？

答：以太坊区块链大概每妙可以完成20到40个交易（以太坊所有的用户形成的交易次数）；当交易达到上限时剩下的用户就需要去竞争以使他们的交易被链打包进去，竞争也使打包的费用升高了（在区块链中，为交易支付的打包费用越高，则越可能会被“矿工”优先打包。）

​	Arbitrum采用乐观Rollup策略，将大部分运算与存储任务移交至L1链下（即L2上）来优化成本。L2大多是运行在单台服务器，也就是排序器（Sequencer/Operator）上的一条链。这种方式在“区块链不可能三角”中舍弃了“去中心化”来换取TPS与成本上的优势，允许L2代替以太坊处理交易指令，从而降低成本（虽然排序器作为系统中枢带有中⼼化色彩，但在成熟度比较高的Rollup方案中，中心化排序器仅能实施交易审查等软性作恶⾏为，或者恶意宕机，但在理想状态的Rollup⽅案中，有相应的⼿段进⾏遏制（比如强制提款或排序证明等抗审查机制））。

#### Arbitrum的原理

答：Arbitrum采用乐观Rollup，这意味着暗含一条信任假设：任意时刻⾄少有⼀个诚实的L2验证者节点。不主动验证提交过来的数据，乐观地认为这些数据没有问题。如果提交的数据有错误，L2的验证者节点会主动发起挑战。挑战过程可概括为可以概括为多轮互动式细分、单步证明。在细分环节，挑战双⽅先对有问题的交易数据进⾏多轮回合制细分，直⾄分解出有问题的那⼀步操作码指令，并进⾏验证。因没有通过验证的L2 Block不具备最终确定性，故验证不通过时排序器可以对这些Block进行回滚。一般而言被提交到Layer1上的L2数据无法回滚，可以具有最终确定性。

### 2024.12.10

<!-- Content_END -->
