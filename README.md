# blockchain-creator
发表以及总结相关文章

## 跨链总结
脾气不好。

### 跨链概述
不同的区块链之间信息交换的基础设施。

跨链桥:支持资产在不同区块链之间专一的系统就是桥。



### 跨链技术难题
原理：
1.哈希锁定。

2.侧链
数据存储会有体积膨胀的问题。

3.公证人机制
amm撮合方式 公证人的信誉存在问题。

4.中级链
Cosmos 和 Polkadot

[关于跨链技术的分析和思考](https://cloud.tencent.com/developer/news/840490)
[什么是跨链（上）](https://learnblockchain.cn/article/2959)
[打造一个跨链 AMM，我们做得到吗？](https://mirror.xyz/0xb54e978a34Af50228a3564662dB6005E9fB04f5a/YC7_2CNPPhkmmOZ_5K61ElY34CrXi4XBw7beGaBv2l8)
[跨鏈橋賽道解析（下）](https://www.grenade.tw/blog/cross-chain-bridge-introduction-2/)





### 跨链目前的实现方式
1.layer0跨链
Polkadot
Cosmos


2.layer1跨链
闪电网络
 RSMC，HTLC。
 要求转账方在指定时间提交转账证明，否则就会将资金退回。
以太坊侧链
NEAR, xDAI network, BSC和Heco都是关注度比较高的以太坊侧链。
信息相互传递。gas费用增多并且验证节点存在安全隐患。

3.amm跨链

4.layer2跨链 （Layer2 Rollup）
 状态通道、Plasma 和 rollup
- zksync协议 -Orbiter Finance roolup之间的桥
    汇总每个批次包含zksync的所有证明，证明执行批次的正确结果。
    *Loopring、StarkWare、Matter Labs ZKSync 和 Aztec 2.0*
 提现
    用户从L2发起提款，在将交易数据编码为字符串后签名并发送交易至L1，交易进入到L1上的zkSync智能合约中，经过提现期限后，证明该区块正确的ZK证明生成并发布到L1上并完成验证，这笔提现就完成了。
 充值
- Arbitrum

- Optimistic
plasm-由于数据安全问题基本上没有实际用途
- layer1扩容 改造链
- layer2跨容 一部分转到链下计算 使用智能合约作为沟通基础

原文链接：
[V神提出的Rollups之间的桥要如何修建](https://www.cngold.com.cn/202106179704736525s29.html)

5.中心化桥
Notary
WBTC
BitGo Trust一边在BTC区块链中托管资产，一边在以太坊上通过运行智能合约来发行WBTC并更新余额。
面临极大的安全问题。


### .典型产品
Across Protocol
基于预言机的layer2-layer1的跨链桥

Allbridge
多生态跨链桥，可提供EVM和**非EVM**跨链桥。
https://allbridge.io/

anyswap
基于smpc多方计算加门签名的去中心化跨链协议
https://anyswap.exchange/#/router

celr bridge
使用哈希锁定，只需要发送一笔的转账，目标链上也是发送一笔转账哈希
https://cbridge.celer.network/

Hop Protocol
基于layer2的原生跨链协议
发行了原生代币hasets 跨链时铸造 结束销毁。
https://app.hop.exchange/send

Nerve Network
基于NULS微服务的跨链框架。
https://bridge.nerve.network/

RenBridge
锁定原生资产的跨链框架。区别于以上的跨链协议。

Ralay Chain
多链跨链桥协议，允许合作伙伴集成自己的产品中。
https://app.relaychain.com/#/cross-chain-bridge-transfer

Connext
注重用户体验的跨链桥协议。
https://www.xpollinate.io/


官方桥:
Horizon-Harmony的官方跨链桥
Optics-celo的官方跨链桥
Optimism Gateway-Optimism的官方跨链桥
Terra Bridge-Terra的官方跨链桥
Wormhole-Solana的官方跨链桥


综合桥
ChainSwap
跨链聚合协议 集合了包括anyswap celr bridge 等跨链桥梁
https://exchange.chainswap.com/


### 跨链模拟实现





###跨链的未来

