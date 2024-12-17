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

# User Trading Flow

### 1. Normal Swap Example: ETH on Ethereum → USDT on BSC

**Route 1: Direct Swap on Ethereum**

**Process：**

* User swaps ETH → USDT directly on Ethereum.

**Factors to Consider:**

* High Ethereum gas fees.
* Slippage due to liquidity conditions.

**Route 2: Cross-Chain Swap via Axelar**

**Process:**

* **Step 1**: User initiates a cross-chain swap from ETH on Ethereum to USDT on BSC.
* **Step 2:** Axelar bridges ETH from Ethereum to Binance Smart Chain (BSC) using its Interchain Messaging Protocol (GMP).
* **Step 3:** The platform executes a token swap (ETH → USDT) on BSC.

**Factors to Consider:**

* Lower gas fees on BSC compared to Ethereum.
* Bridging fees incurred via Axelar.

***

### 2. Limit Order Example: BTC on THORChain → ETH on Ethereum

**Route 1: Direct Limit Order on THORChain**

**Process：**

* User sets a limit order to swap BTC → ETH on THORChain.
* THORChain’s native price feeds monitor the market price of BTC and ETH.
* Once the specified price condition is met, the limit order is executed.

Factors to Consider:

* Native asset support on THORChain (no need for wrapped BTC or ETH).
* Low slippage due to deep liquidity pools.

**Route 2: Cross-Chain Limit Order via Axelar**

**Process:**

* **Step 1:** User places a limit order to swap BTC on THORChain → ETH on Ethereum.
* **Step 2:** Axelar bridges BTC from THORChain to Ethereum once the price condition is met.
* **Step 3:** The platform swaps BTC → ETH on Ethereum.

**Factors to Consider:**

* Bridging fees and Axelar relayer costs.
* Ethereum gas fees for executing the final swap.

***

### 3. Auto-DCA Example: USDT on BSC → ETH on Ethereum

**Route 1: Periodic Swaps on BSC**

**Process:**

* User schedules Auto-DCA purchases to buy ETH with USDT periodically on BSC.
* The platform swaps USDT → ETH on BSC.

**Factors to Consider:**

* Lower transaction fees on BSC.
* Potential price variations during each scheduled purchase.

**Route 2: Cross-Chain Auto-DCA via Axelar**

**Process:**

* **Step 1:** User configures Auto-DCA to purchase ETH on Ethereum using USDT on BSC.
* **Step 2:** On each interval, Axelar bridges USDT from BSC to Ethereum.
* **Step 3:** The platform swaps USDT → ETH on Ethereum.

**Factors to Consider:**

* Bridging fees and Axelar gas costs for each interval.
* Higher Ethereum gas fees for executing swaps.
* Execution intervals ensure cost-averaging but can accumulate gas costs over time.

***

### Cost Estimation & Execution

#### Normal Swap Cost Comparison

**Route 1 (Direct on Source Chain):**

* Swap Fee: Platform-specific fee, if any.
* Gas Fee: High Ethereum gas costs.

**Route 2 (Cross-Chain):**

* Bridging Fee: Gas costs for Axelar bridge + relayer fee.
* Gas Fee: Lower BSC transaction costs.

#### Limit Order Cost Comparison

**Route 1 (Direct on THORChain):**

* No additional fees for bridging or wrapping.

**Route 2 (Cross-Chain):**

* Bridging Fee: Axelar costs for cross-chain transfer.
* Gas Fee: Ethereum gas costs for executing the swap.

#### Auto-DCA Cost Comparison

#### Route 1 (Single-Chain):

* Gas Fee: Lower BSC transaction costs for each interval.

**Route 2 (Cross-Chain):**

* Bridging Fee: Axelar costs for each transfer interval.
* Gas Fee: Ethereum gas costs for executing swaps.

**Execution:**

* The platform calculates and ranks routes based on total costs, slippage, and speed.
* The best route is selected, and trades are executed seamlessly via the Smart Routing Engine.
