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

Yi

1. 各位老师好，我是 Yi , 两年经验的后端开发(Java向)，很高兴认识大家
2. 个人时间相对充裕，有接触新知识的欲望，我认为我可以完成此次学习

## Notes

<!-- Content_START -->

### 2024.12.10

>Ethereum:
>
>Ethereum 吞吐量低的原因
>
>1. 每个节点都会参与处理历史的每一笔交易
>2. 为了做到去中心化，Ethereum 需要大多数人可以运行（对用户硬件配置和软件资源的要求比较低）
>
>

>Arbitrum（Rollup、Arbitrum One）
>
>简介
>
>Arbitrum 是为了解决以太坊 Tps 低的问题而开发的项目，它通过 **Rollup** 协议在以太坊之上创建了一个交易层。
>
>最终 Arbitrum 会将将交易数据打包发布到以太坊，保证了项目的安全性和去中心化的同时，提高了处理速度。
>
>
>
>特点
>
>1. 更高的吞吐量（更快的交易确认）
>2. 更低的费用
>
>
>
>安全性
>
>从简介中来看，只要有一个诚实的用户，就能证明任意数量的欺诈者（此处推测，验证器可能是利用 Ethereum 的账本机制，来回溯真实的交易记录）
>
>
>
>兼容性
>
>从用户的角度，基本上与使用 Ethereum 没有区别；
>
>从开发人员的角度，工具和库都兼容，而且在保持兼容性的前提下，支持用 Rust、C++ 来编写高性能的智能合约

>AnyTrust（Nova）
>
>Rollup 链的所有数据放在 L1 链上管理，而 AnyTrust 链的数据，放在链下管理，在遇到攻击时，AnyTrust 链会恢复到 Rollup 的模式，但是这里需要至少 2 名成员是诚实的。
>
>数据放在链下，吞吐量会进一步提高，用户费用也会显著减低，适合高吞吐量且不需要完全去中心化的应用

### 2024.12.10

<!-- Content_END -->
