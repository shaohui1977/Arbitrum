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

### 2024.12.11

>交互式证明:
>
>争议双方参加一个由 L1 合约引导的回合制协议，双方在链下进行争议的解决
>
>如果该争议涉及了 N 个执行步骤，一方曝光出 2 个涉及 N/2 的断言，然后让对方选择一个挑战，这样争议规模就缩小了一半；重复以上步骤，直至争议缩减到单个执行步骤，此时再到链上按此步骤执行来解决争议
>
>
>
>重执行证明:
>
>让一个 Rollup 区块在区块内每一笔交易上做断言，L1 引导合约模拟执行整个交易流程，来验证结果

>交互式证明的优势:
>
>1. 效率更高
>
>乐观情况下，一个区块只需要包含一个断言，空间占用小，节省成本。
>
>悲观情况下，引导合约只需要执行一个步骤即可验证争议，速度快
>
>2. 更高的交易级 gas limit
>
>交互式证明的 gas limit 相较于 Ethereum 要大得多，重执行证明受限于 Ethereum 的 gas limit，可能没办法在一笔交易内模拟执行完
>
>3. L2 上的合约大小没有限制
>
>交互式证明不需要为 L2 合约在 Ethereum 上创建对应合约，所以不受限制；重执行模式的 gas limit 必须小于 Ethereum 合约的 gas limit（因为模拟执行的 gas limit 消耗更大）
>
>4. 灵活性
>
>举个例子，EVM 中新增指令，必要的功能无非是能在以太坊上验证一个单步执行的证据。而重执行模式就严格受限于 EVM

>Arbitrum 欺诈证明：
>
>1. 从全局状态开始，进行二分查找，将争议缩小至单个区块
>2. 在区块内部调用 ChallengeExecution，同样二分查找判定，将争议缩小至单个步骤
>3. 提供证明数据，调用 oneStepProveExecution，验证结果
>
>争议以两个段作为开始，此时假设双方同意某一段的正确性，对第二段存在分歧；下一轮中，选择第一段作为起始，结尾位置在上一轮第二段之前，此时就将争议缩小了一部分；重复以上流程，直至争议缩减至单个步骤，解决争议。（每一轮中，双方轮流决定挑战的位置）
>
>赢得挑战后，挑战方不能做出任何有效行动，最终会因为超时而失败，这样做是为了预防，如果挑战被错误解决，就有时间通过合约升级来诊断和修复错误



### 2024.12.12

>Arbitrum Classic:
>
>首次在 Arbitrum One 链主网上发布的技术
>
>
>
>Arbitrum Nitro:
>
>Arbitrum 最新的技术，是 Arbitrum Classic 的升级
>
>
>
>相同点:
>
>两者都创建了一个尽可能接近 EVM 的执行环境，作为 L2;
>
>通过以太坊本身简洁的欺诈证明来保证 L2 的安全性
>
>
>
>不同点:
>
>Classic 通过定制虚拟机（AVM）来实现，虚拟机上运行 ArbOs，可以模拟 EVM 的执行
>
>Nitro 通过 Go 语言实现逻辑，在欺诈证明的时候编译成 Wasm 来执行

>Nitro 的优势:
>
>1. 费用更低
>
>Classic 中，高级语言（solidity，vyper）会被转化为 EVM 字节码，然后 ArbOs 会将 EVM 字节码转换为相应的 AVM 指令在 L2 链上运行，这些 AVM 指令可以作为证明欺诈的输入。在交互式欺诈证明中，找到 AVM 中的一步证明，然后在 EVM 中执行
>
>Nitro 中，L2 链上运行的 Go 代码。Nitro 会定时生成类似 Ethereum 的区块，这些区块可以视为 Check Point。利用这点，将交互式欺诈分为 2 个阶段：首先将争议缩小到一个区块上，然后把该区块代码编译为 Wasm，再把争议缩小至 Wasm 指令。所以只能再发生争议时，才需要将 Go 编译成 Wasm 来证明欺诈。
>
>大多数正常情况下在 L2 链上使用 Go 代码来执行，仅在需要欺诈证明时编译成 Wasm 去 EVM 上证明欺诈，这种方式速度更快，性能更强，相应的，费用也就越低
>
>
>
>Arbitrum 交易的大部分费用都用于支付在 Ethereum 上发布数据的成本，所以如何压缩数据就非常关键。
>
>Classic 中，AVM 是为 Arbitrum 定制的虚拟机，压缩算法需要自定义并且手动实现，有很高的技术风险
>
>Nitro 中，使用 Go 代码，可以使用成熟的压缩库，显著降低发布交易到 L1 上的成本
>
>
>
>
>
>2. 兼容性更强
>
>ArbOs 虽然能处理所有的 EVM 操作码，但还是有些逻辑与 EVM 不同，比如：gas 费的单位不同导致 L1 上的合约必须经过修改逻辑之后才能发布到 L2 上，很不方便；
>
>Nitro 用 Go 模拟 Ethereum 运行，基本一比一复刻
>
>
>
>
>
>3. 简洁性
>
>AVM 是定制的，没有对应的高级语言，开发成本比较高；
>
>Nitro 用 Wasm 作为 L2 的虚拟机，可以用高级语言进行编写合约，代码要精炼、简单很多，开发成本更低，安全性也更加有保障

### 2024.12.13

>AnyTrust:
>
>AnyTrust 是 Nitro 的技术变式，它通过最小信任假设来降低交易成本，依靠链下数据可用性委员会来存储数据和证明欺诈
>
>
>
>数据可用性委员会:
>
>AnyTrust 模式下，用户将交易发布到 Sequencer 之后，Sequencer 会将数据发到链下委员会存储，委员会将为批量的交易数据签署可用性证书（DACerts），只有 DACerts 会被上传到主网的 inbox 合约，进一步降低了发送到主网的数据大小。而且委员会公开了查询接口，允许通过证书的 Hash 获取数据批次。
>
>当需要获取交易数据的时候，从 inbox 合约中获取上传的 hash 值，通过查询接口，就可查询到交易数据。Anytrust 方案在一定程度上牺牲了去中心化特性（也牺牲了一定安全性），依赖中心化组织保证数据的正确性
>
>
>
>Nova:
>
>Nova 是基于 AnyTrust 技术搭建的新链，专为游戏、社交应用程序这种对成本和性能更敏感的应用而设计。	Nova 支持了 2 种数据发布方式，一种是以 Calldata 的形式发布完整数据，一种是发布 DACert 的方式。
>
>Nova 的定序器将完整的数据集同时发送给所有 DAC 委员会的成员，委员会签名后把带有签名的证明返回给定序器，定序器收集到足够多的证明就能将它们聚合并创建有效的数据可用性证明（DACert），然后把 DACert 发布到主网。如果定序器没有收集到足够多的证明，Nova 会回退到 Rollup 模式（以 Calldata 形式发布数据到主网）。

>Orbit：
>
>Orbit 是一个开发框架，允许用户使用任何基于 Arbitrum Rollup 的 L2 网络作为结算层来创建和启动 L3 网络。借助 Arbitrum Orbit，用户可以在隐私、权限、费用代币、治理等方面定制自己的链。（L3 使得链上资源密集型应用成为可能。）
>
>
>
>BOLD：
>
>BOLD 是 Arbitrum 团队提出的无需许可验证机制，目的是最小化结算状态的延迟。
>
>目前对于乐观 Rollup 而言，普遍存在一周的挑战期，用户从 L2 提现到 L1 要等一周；挑战期内验证者如果发现提交上来的 L2 交易有问题，可以发起挑战。
>
>通过引入 BOLD 机制，一方面能实现验证的无需许可，更符合区块链去中心化的理念；另一方面，能实现最小化结算状态的延迟。BOLD 允许单个诚实的验证者在以太坊上与任意数量的对手进行争议时取胜，从而使 DDOS 攻击失效。
>
>
>
>Stylus：
>
>简言之，开发人员在 Arbitrum 上既能使用传统 Solidity 语言，又能使用 WASM 兼容的语言，如 Rust、C 和 C++ 等来构建应用程序。此外，Stylus 使 Dapps 的执行更加高效，显著地降低了 gas 成本。

<!-- Content_END -->
