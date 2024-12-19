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

# Oracles

### Introduction

Oracles are integral to Allswap’s advanced functionalities, such as limit orders and Auto-DCA (Dollar Cost Averaging), ensuring accurate and reliable price data for seamless trading execution. In addition to traditional oracles like Chainlink and Pyth, THORChain’s native price feeds enhance the platform’s ability to manage native asset swaps with deep liquidity.

***

### Limit Orders

#### Price Feed Oracles

To ensure accurate and reliable price data, our platform leverages multiple oracle solutions for redundancy and optimal performance:

**Primary Oracles:**

* Chainlink and Pyth provide real-time price feeds for high-accuracy limit order execution.
* THORChain’s native pricing mechanism is used for native asset swaps to reflect actual liquidity pool prices directly.

**Fallback Oracles:**

* Time-Weighted Average Price (TWAP) mechanisms on DEXs like Uniswap, Curve, Raydium, and Orca serve as secondary data sources.
* For native swaps, fallback pricing can be derived from alternative THORChain-compatible price feeds.

**Oracle Resilience:** Redundant systems, including THORChain’s native pricing, ensure continued operation and accurate pricing in case of primary oracle failures.

#### Execution Mechanism

Oracles continuously monitor prices to trigger the fulfillment of limit orders through secure smart contracts.

**Key Steps:**

1. **Price Monitoring:** Oracles (e.g., Chainlink, Pyth, THORChain) track the market price for the target asset.
2. **Condition Verification:** Limit order conditions are checked against the monitored price.
3. **Order Fulfilment:** Once the price condition is met, smart contracts execute the trade securely.
4. **Fallback Mechanisms:** TWAP pricing or alternative oracles ensure uninterrupted order execution in case of oracle outages.

***

### Auto-DCA Function

#### Order Scheduling

The Auto-DCA function allows users to automate periodic asset accumulation across multiple chains and assets, including those on THORChain.

**Features:**

* **Flexible Intervals:** Users define the frequency of purchases (e.g., daily, weekly).
* **Native Asset Support:** THORChain’s price feeds allow for DCA purchases directly using native assets like BTC, ETH, or RUNE.
* **Partial Fills:** Supports partial order execution when price conditions align, enabling cost-effective accumulation over time.

#### Oracle Dependency

The Auto-DCA function extends oracle integration for recurring orders across various chains:

* **Price Monitoring:** Oracles, including THORChain, track real-time prices to determine the best execution times.
* **Native and Bridged Assets:** Ensures accurate pricing for both native assets (via THORChain) and bridged assets (via Chainlink, Pyth).
* **Seamless Integration:** Recurring orders use the same reliable oracle-based logic as limit orders, with additional support for native swaps.

***

### Why Oracle Integration Matters

Our platform’s robust oracle integration ensures:

* **Accuracy:** Combines Chainlink, Pyth, and THORChain feeds for precision trading.
* **Resilience:** Redundant systems prevent data outages from disrupting trades.
* **Native Asset Support:** Leverages THORChain’s pricing for deep liquidity and accurate native asset valuations.
* **Automation:** Enables advanced features like limit orders and Auto-DCA with minimal user intervention.

\\
