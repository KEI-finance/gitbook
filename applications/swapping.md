---
description: Simplifying the user experience
cover: ../.gitbook/assets/Screen Shot 2023-05-25 at 10.46.33.png
coverY: 0
---

# 🔄 K-swap: Advanced Swapping

## <mark style="color:purple;">**Custom SwapRouter: Multi-Source Token Purchase**</mark>

Kei Finance integrates a proprietary SwapRouter within its system architecture, designed to amplify the user trading experience. The core function of this SwapRouter is to facilitate the purchase of KEI tokens from multiple pools and dynamically select the most beneficial prices. This user-centric feature eliminates the need for manual pool selection and ensures the acquisition of KEI at the best possible price, without additional effort from the user.

## <mark style="color:purple;">**Best Price Selection: Smart Pool Comparison**</mark>

The SwapRouter incorporates an intelligent price comparison mechanism. This feature compares the price of the Uniswap pair and the Supplier, subsequently routing the purchase transaction towards the pool offering the best price value. By doing so, the SwapRouter guarantees that users get the maximum KEI for their spent assets, optimizing value extraction from each transaction.

## <mark style="color:purple;">**Automated Buyback and Burn: Ensuring Price Stability**</mark>

If the KEI token price dips below the defined floor price during a transaction, the protocol instantaneously purchases the tokens back and initiates a burn process. This action reduces the total supply of KEI, which counteracts the price drop and restores the token's price back up to the floor level. This automated buyback-and-burn mechanism ensures the sustained stability of the KEI token price, minimizing the impact of market volatility on the Kei Finance ecosystem.

## <mark style="color:purple;">**Affiliate Tracking: Rewarding Community Contribution**</mark>

The SwapRouter is not merely a tool for trade optimization; it also serves a crucial role in the Kei affiliate program. As each swap transaction is conducted, the SwapRouter records the transaction's affiliate, enabling the protocol to keep a meticulous record of affiliate contributions. This feature fosters a sense of community and shared profit, as it enables affiliates to receive deserved rewards for their contributions to the Kei Finance ecosystem.
