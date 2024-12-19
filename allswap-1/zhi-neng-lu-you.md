---
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

# 智能路由

## 资产桥接&#x20;

Axelar 的跨链代币服务 (ITS) 和 THORChain 的原生交换基础设施为跨链资产移动提供了无与伦比的灵活性。

## 方法

• 自动化桥接： Axelar 处理代币桥接，无需人工干预，而 THORChain 促进原生资产的直接交换。&#x20;

• 成本效益： 路由逻辑考虑桥接费用、包装/解包装成本（针对 Axelar）和直接交换成本（针对 THORChain）。&#x20;

• 扩展兼容性： 确保 EVM 链、非 EVM 链和 THORChain 上的原生资产之间的无缝交互。

## 路由流程工作流

1\. 输入收集： 用户指定源/目标代币、数量和滑点容忍度。&#x20;

2\. 流动性数据获取： 从 DEX（如 Uniswap、SushiSwap）、Axelar、Squid Router 和 THORChain 获取实时数据。&#x20;

3\. 路径发现： 识别 Axelar、Squid Router 和 THORChain 上的单链、多链和原生路径。&#x20;

4\. 成本估算： 按总成本、滑点、执行速度和原生交换收益对路径进行排名。&#x20;

5\. 执行：&#x20;

• 对于单链交易： 直接在最佳 DEX 上执行。&#x20;

• 对于多链交易： 利用 Axelar 和 Squid Router。&#x20;

• 对于原生资产交换： 使用 THORChain 的深度流动性进行高效执行。

## 优化策略

&#x20;• 预计算路径： 缓存频繁交易的路径，包括桥接资产和原生资产，以减少延迟。&#x20;

• TWAP 监控： 检测 Axelar、Squid Router 和 THORChain 流动性池中的价格操纵行为。

***

## 为何选择 THORChain？&#x20;

THORChain 通过以下方式为我们的基础设施带来显著价值：&#x20;

• 原生资产支持： 避免使用包装资产，直接访问原生代币流动性。&#x20;

• 深度流动性： 减少高价值交易的滑点。&#x20;

• 弹性路由： 当原生交换提供更好性能时，作为 Axelar 和 Squid Router 的替代方案。
