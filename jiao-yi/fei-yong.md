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

# 费用

**简介**

高效的 Gas 费用管理对于实现跨链交换的无缝用户体验至关重要，也是 KYEX 在为用户构建 Allswap 时的核心考虑之一。通过利用 **Axelar 的 Gas 抽象服务** 和 **THORChain 的原生流动性模型**，用户可以享受简化的费用处理流程并减少操作复杂性。

***

#### Gas 费用与抽象

**Axelar 的 Gas 抽象服务**

Axelar 的 Gas 服务允许用户在源链上通过单笔交易预付所有必要的 Gas 费用，从而简化跨链交换。

**主要特点：**

* **单一货币支付 Gas：**\
  用户只需用源链的原生代币支付 Gas 费用，无需持有多个链的 Gas 代币。
* **自动费用管理：**
  * 服务根据实时汇率计算所有相关链的 Gas 成本。
  * 动态分配费用至 Axelar 和目标链。
* **退款机制：**
  * 未使用的 Gas 费用将在交易完成后退还到用户的源链账户。

**工作原理：**

1. 用户在源链上发起交易，指定代币和目标链。
2. Gas 费用用源链代币预先计算并支付。
3. Axelar 自动将所需的 Gas 费用分配到交易涉及的所有链上。
4. 未使用的 Gas 费用在交易完成后退还。

***

**THORChain 的费用模型**

THORChain 提供原生资产流动性模型，使用户可以直接执行交换，且费用结构简单明了。

**主要特点：**

* **固定流动性提供者费用：**
  * 交换涉及的流动性费用是根据资金池深度和交易规模确定的固定费用。
* **原生资产交换：**
  * 无需封装代币，确保 Gas 和交换费用更直观。
* **Gas 优化：**
  * Gas 费用直接从原生资产的交易金额中扣除。

**工作原理：**

1. 用户在 THORChain 的流动性池中直接交换原生资产。
2. Gas 费用在交换资产中自动包含并扣除。
3. 透明的费用结构让用户清楚知道被扣除的确切金额。

***

#### 用户的优势

* **简化的 Gas 支付：** 一次性使用单一代币支付所有交易费用。
* **透明的费用结构：** 了解确切的费用扣除，没有隐藏成本。
* **高效的跨链交换：** 降低处理多个链和代币的复杂性。