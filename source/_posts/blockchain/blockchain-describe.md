---
title: "白话区块链"
date: 2017-08-18 14:17:39
categories: blockchain
tags:
  - blockchain
---

### 定义

    这里将区块链定义为：分布式的共享账本，具有去中心化、点对点通讯、共识机制、加密算法等特征。

### 历史

    自 2008 年神人**中本聪**发表比特币白皮书以来，人们对比特币背后的区块链技术愈发感兴趣，这也导致区块链技术快速发展。如果说[比特币][bitcoin]代表了第一代区块链技术，那[以太坊][ethereum]可以称之为第二代区块链技术，智能合约的出现将区块链的应用范围大大扩展，不再限于发行、交易数字货币，而是可以应用于各行各业，如金融，博彩，存证等。可以预见，随着区块链技术的发展，去中心化应用将会占据越来越大的空间。

### 主要组件

    - 通讯层
      通讯层是指区块链网络中各节点间的通讯方式。由于区块链网是一个去中心化的网络，没有特定哪个节点是网络的中心服务器，反而是网络中的每个节点既是客户端，也是服务器，_我为人人，人人为我_，每个节点都是平等的，非常像以前 BT 网络，区块链的底层通讯协议也正是建立在 P2P 协议上。

    - 数据层
      同理，区块链网络中没有特定的中心服务器，那数据是存放在哪的呢？答案是存在每一个节点上，每个节点上的数据都是一样的，是全网同步的，这即是所谓的分布式共享账本。共享的涵义有 2 层，1 是每个节点都可以查看账本，2 是每个节点都可以参与记账。

    - 共识层

      - 什么是共识？共识即某些人对某件事得到统一的结论，在区块链上是对账本的内容达成共识。在区块链网络中，每秒都会发生大量的交易，这些交易能否生效，谁先谁后，如何避免*双花(同 1 笔钱共 2 次)*等，这都是共识要考虑的问题。

      - 如何达成共识？这里要依赖共识算法，如典型的共识算法 POW(工作量证明)，什么是工作量证明？在职场中，我们看你有没有学士文凭来验证你是否上过大学，通过查看房间是否卫生来确定是否已经打扫过，这就是工作量证明。在比特币网络中，在所有节点上通过计算[hash 谜题][hash]来竞争，计算[hash 谜题][hash]的过程就是一种工作量证明，只有最快完成工作的节点才拥有记账权，一旦某个节点完成 hash 计算，则本轮竞争结束，重新开始下一个循环。比特币正是由这一个又一个的循环来完成区块链的记账过程的，在每一个循环过程中，最先完成计算，获得记账权的节点会获得一定数量的比特币，这就是在挖矿，这个节点此时叫矿工。

### 可选组件

    - 激励层

### 分类

    根据区块链是否公开，可以将区块链私链和公链。

        * 公链，任何节点都可以随时加入或退出，一般不需要身份验证，隐私性比较强，如[比特币][bitcoin]，[以太坊] [ethereum]，[小蚁][neo]，因为对节点的身份不做限制，也就是说节点间是互相不信任的

        * 私链，私链一般用在数据需要保密，对网络中节点有身份认证的要求，常见于企业与企业之间，或是部门与部门之间，节点之间彼此相信，如[超级账本][hyperledger]。

### 智能合约

    - 什么是智能合约
      传统合约是以纸质的形式签订，是否履行也依赖于人的主观性。智能合约本质上是一段电脑程序，合同条款以数字形式保存，在满足一定条件时自动触发执行。可以想像，这种方式将会减少多少*老赖*。

    - 智能合约用途
      - 发行代币，这是区块链的老本行，不能忘。
      - 数据上链，比如说存款，链上仅提供设置余额的功能
      - 业务上链，还是说存款，链上还要提供存、取功能，取的时候要判断是否余额足够等情况。

[ethereum]: https://www.ethereum.org/
[bitcoin]: https://bitcoin.org/
[hash]: http://www.infoq.com/cn/articles/bitcoin-and-block-chain-part02
[neo]: http://neo.org
[hyperledger]: https://www.hyperledger.org/
