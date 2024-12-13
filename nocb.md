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

# Hansen

1. 虽然很早就了解过arb，但没有系统的学习和使用过。
2. 你认为你会完成本次残酷学习吗？  应该可以完成 ，抽时间学习 

## Notes

<!-- Content_START -->

### 2024.12.10

#### ARB基础介绍

- ARB is Optimistic rollup protocol ，is a L2  
- L2 是为了Ethereum的扩容
- L1 保证了L2的安全性，
- The only delay that's felt by a user is in "withdrawing" — moving their funds from Arbitrum back to Ethereum;
- 批次，压缩 ，所以L2的费用低和效率高
- 最新技术栈：Stylus ，可以支持 rust 

### 2024.12.11

- ARB have 2 chain ，Arbitrum One   and  Nova. Orbit can create L3
- Arbitrum DAO  

#### Arbitrum suite

The Arbitrum suite includes the protocols, chains, services, and SDKs that power the Arbitrum ecosystem:

Arbitrum Rollup:	A protocol for scaling Ethereum smart contracts.
Arbitrum AnyTrust	A protocol for scaling Ethereum smart contracts even further, with a mild trust assumption.
Arbitrum Nitro	The node software that codifies the Rollup and AnyTrust protocols.
Arbitrum nodes	Machines that run Nitro in order to service and/or interact with an Arbitrum chain.
Arbitrum One	A public Rollup chain.
Arbitrum Nova	A public AnyTrust chain.
Arbitrum bridge	Lets you move ETH and ERC-20 tokens between Ethereum, Arbitrum, and select Orbit chains.
Arbitrum Orbit	Lets you run your own Rollup and AnyTrust chains.
Arbitrum Stylus  write contract with rust  

- 用户通过bridge ，dapp 来使用arb 
- 开发者可以使用  solidity and rust 语言  
- 矿工 运行全节点 nitro 
- 通过orbit 可以创建自己的 L3  

#### chain info  

- 介绍了 RPC 的地址 和特点 
- 介绍了一些共用的 rpc provider  
- 介绍了 几个重要的合约地址 ，及欺诈证明合约 ，bridge ，及水龙头

### 2024.12.12

#### 创建Dapp 
- ui -> provider -> node -> contract
- 就像前后端分离一样，   ui 是前端， 合约是服务， 用solidity 语言写，部署在去中心化网络。

### 2024.12.13
#### run Arbitrum node 
- 节点类型：  full node， archive node，classic node 

一般运行full 节点 就可以了 ， 比归档节点要省资源， 

- Nitro ，full node  
	- hardware： 普通的电脑即可 
	- 可以用docker 
	- snapshot  可以快速同步  
	- 也有rpc 的接口 
	- 需要和 L1 的接口对接 

- 创建一个本地的为开发用的 虚拟链 
- L1 provider  
	- data stored in blob ，on the beacon chain. 

### 2024.12.14

### 2024.12.15

### 2024.12.16

<!-- Content_END -->
