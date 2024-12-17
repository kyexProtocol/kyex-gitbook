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

# Smart Routing

### Asset Bridging

Axelar’s Interchain Token Service (ITS) and THORChain’s native swap infrastructure provide unparalleled flexibility in moving assets across chains.

**Methodology:**

* **Automated Bridging:** Axelar handles token bridging without manual intervention, while THORChain facilitates direct swaps for native assets.
* **Cost Efficiency:** Routing logic factors in bridging fees, wrapping/unwrapping costs (for Axelar), and direct swap costs (for THORChain).
* **Expanded Compatibility:** Ensures seamless interaction between EVM chains, non-EVM chains, and native assets on THORChain.

***

### Routing Process Workflow

1. **Input Collection:** User specifies source/target tokens, amounts, and slippage tolerance.
2. **Liquidity Data Fetching:** Fetches real-time data from DEXs (e.g., Uniswap, SushiSwap), Axelar, Squid Router, and THORChain.
3. **Route Discovery:** Identifies single-chain, multi-chain, and native routes across Axelar, Squid Router, and THORChain.
4. **Cost Estimation:** Ranks paths by total cost, slippage, execution speed, and native swap benefits.
5. **Execution:**

* For single-chain trades: Executes directly on the best DEX.
* For multi-chain trades: Leverages Axelar and Squid Router.
* For native asset swaps: Utilizes THORChain for deep liquidity and efficient execution.

**Optimization Strategies:**

* **Precomputed Routes:** Caches frequently traded paths involving both bridged and native assets for reduced latency.
* **TWAP Monitoring:** Detects price manipulations across Axelar, Squid Router, and THORChain liquidity pools.

***

### Why THORChain?

THORChain adds significant value to our infrastructure by enabling:

* **Native Asset Support:** Avoids the need for wrapped assets, providing direct access to native token liquidity.
* **Deep Liquidity:** Reduces slippage for high-value trades.
* **Resilient Routing:** Acts as an alternative to Axelar and Squid Router when native swaps offer better performance.
