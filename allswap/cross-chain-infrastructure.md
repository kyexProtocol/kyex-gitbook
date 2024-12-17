---
description: Introduction
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

# Cross-Chain Infrastructure

### Introduction

KYEX’s Allswap leverages multiple cross-chain protocols, as well as unified liquidity protocols to allow users to access various assets and their pools, regardless of which chain they are on, be it receiving native assets or wrapped assets.&#x20;

To start with, KYEX will first be implementing Axelar, with the combined reach of Axelar’s Interchain Token Service (ITS), as well as Squid Router, followed by the implementation of THORChain for added support of native asset swaps with deep liquidity. Axelar's interchain communication to deliver seamless, efficient, and secure cross-chain trading. With high performance and scalability, KYEX enables optimal trading experiences across multiple blockchains.

***

### Cross-Chain Swap Trading

#### Smart Routing Engine

The Smart Routing Engine powers cross-chain swaps by analyzing liquidity, gas costs, price impacts, and native asset support.

**Key Features:**

* **Liquidity Pool Analysis:** Aggregates and evaluates liquidity from DEXs like Uniswap, Curve, PancakeSwap, and THORChain pools.
* **Routing Optimization:** Selects the most efficient route by incorporating gas costs, execution speed, and fallback mechanisms.
* **Cross-Chain Compatibility:** Integrates Axelar’s GMP, Squid Router, and THORChain for native and multi-chain routing.

**Axelar and THORChain Integration:**

* **Axelar Network:** Handles interchain messaging and token bridging with sub-1 second latency, high throughput, and robust security.
* **THORChain Integration:** Supports native asset swaps directly between chains with access to deep liquidity pools, eliminating the need for wrapped assets.
* **Dynamic Path Selection:** The engine dynamically decides between Axelar, Squid Router, or THORChain depending on which offers the best route for a given swap.

**Architecture Overview:**

1. **Pathfinding Logic:** Identifies and ranks efficient routes for swaps, including THORChain's native swaps.
2. **Liquidity Aggregation:** Splits large orders across multiple pools, including THORChain’s deep liquidity pools, to reduce price impact.
3. **Dynamic Gas Optimization:** Optimizes gas fees for each transaction step, prioritizing cost-effective paths.
4. **Fallback Mechanisms:** Reroutes seamlessly between Axelar, Squid Router, and THORChain in case of failures or congestion.
