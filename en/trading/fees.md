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

# Fees

### Introduction

Effective gas fee management is critical to creating a seamless user experience for cross-chain swaps, and a top priority in KYEX’s consideration when building Allswap for users. By leveraging Axelar's Gas Abstraction Service and THORChain's native liquidity model, users can enjoy simplified fee handling and reduced operational complexity.

***

### Gas Fees and Abstraction

#### Axelar’s Gas Abstraction Service

Axelar's Gas Service allows users to prepay all necessary gas fees in a single transaction on the source chain, streamlining cross-chain swaps.

**Key Features:**

1. **Single-Currency Gas Payment:**

* Users pay gas fees in the source chain’s native token, eliminating the need to hold multiple gas tokens across chains.

2. **Automated Fee Management:**

* The service calculates gas costs for all chains involved, using real-time conversion rates.
* Allocates fees dynamically to Axelar and destination chains.

3. **Refund Mechanism:**

* Unused gas fees are refunded to the user’s account on the source chain after the transaction completes.

**How It Works:**

* Users initiate a transaction on the source chain, specifying the token and destination.
* Gas fees are calculated and prepaid in the source chain’s token.
* Axelar automatically distributes the necessary gas fees to all chains involved in the transaction.
* Any unused gas is refunded after completion.

***

#### THORChain’s Fee Model

THORChain provides a native asset liquidity model, enabling users to execute swaps directly with minimal fee complexity.

**Key Features:**

1. **Flat Liquidity Provider Fees:**

* Swaps involve a fixed liquidity fee determined by the pool’s depth and transaction size.

2. **Native Asset Swaps:**

* Eliminates the need for wrapped tokens, ensuring gas and swap fees are straightforward.

3. **Gas Optimization:**

* Gas fees are calculated and deducted directly from the transaction amount in the native asset.

**How It Works:**

* Users swap native assets directly in THORChain’s liquidity pools.
* Gas fees are automatically included and deducted in the swapped asset.
* Transparent fee structures allow users to know the exact amount being deducted for gas and liquidity.

***

### Benefits to Users

* **Simplified Gas Payments:** Pay once in a single token for all transaction fees.
* **Transparent Fee Structure:** Know the exact fees being deducted without surprises.
* **Efficient Cross-Chain Swaps:** Reduced complexity for handling multiple chains and tokens.
