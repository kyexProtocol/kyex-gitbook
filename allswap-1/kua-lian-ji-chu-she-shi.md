---
description: 简介
icon: merge
layout:
  title:
    visible: true
  description:
    visible: false
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
---

# 跨链基础设施

## 简介

KYEX 的 Allswap 利用多个跨链协议以及统一的流动性协议，使用户能够访问各种资产及其流动性池，无论它们位于哪个区块链上，无论是接收原生资产还是包装资产。

首先，KYEX 将实现 Axelar，其结合了 Axelar 的跨链代币服务 (ITS) 和 Squid Router 的功能，随后会引入 THORChain，以进一步支持具有深度流动性的原生资产交换。Axelar 的跨链通信提供无缝、高效和安全的跨链交易。凭借高性能和可扩展性，KYEX 在多个区块链上实现了最佳的交易体验。

***

## 跨链闪兑交易

智能路由引擎 智能路由引擎通过分析流动性、Gas 成本、价格影响和原生资产支持来实现跨链交换。

## 主要功能

• 流动性池分析： 聚合并评估来自 Uniswap、Curve、PancakeSwap 和 THORChain 等 DEX 的流动性。&#x20;

• 路由优化： 通过结合 Gas 成本、执行速度和备用机制选择最有效的路径。&#x20;

• 跨链兼容性： 集成 Axelar 的 GMP、Squid Router 和 THORChain，实现原生和多链路由。

## Axelar和THORChain的集成

• Axelar 网络： 处理跨链消息传递和代币桥接，具有亚秒级延迟、高吞吐量和强大的安全性。&#x20;

• THORChain 集成： 支持跨链直接的原生资产交换，访问深度流动性池，无需使用包装资产。&#x20;

• 动态路径选择： 引擎动态在 Axelar、Squid Router 或 THORChain 之间选择，以确定给定交换的最佳路径。

## 架构概述&#x20;

1\. 路径查找逻辑： 识别并排名高效的交换路径，包括 THORChain 的原生交换。&#x20;

2\. 流动性聚合： 将大额订单拆分至多个流动性池（包括 THORChain 的深度流动性池），以减少价格影响。&#x20;

3\. 动态 Gas 优化： 优化每笔交易步骤的 Gas 费用，优先选择成本效益高的路径。&#x20;

4\. 备用机制： 在 Axelar、Squid Router 和 THORChain 出现故障或拥堵时无缝重新路由。
