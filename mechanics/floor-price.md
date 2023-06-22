---
description: Understand how the KEI token increases the protocol's floor price
cover: ../.gitbook/assets/whitepaper-header.png
coverY: 0
---

# Floor Price

## Floor Price Mechanism

KEI Finance utilises a unique and groundbreaking "Raising Floor Price" mechanism, distinguishing it from other DeFi protocols and promoting the stability and growth of the KEI token's value. This innovative method creates a floor price - a minimum value that the KEI token cannot fall below, maintained by a continuous automated buyback and burn process.

<figure><img src="../.gitbook/assets/image (37).png" alt=""><figcaption><p>Constantly raising floor price</p></figcaption></figure>

### Buyback Mechanism

When a user conducts a buy or sell transaction, our algorithm evaluates the current pool price against the floor price. If the pool price falls below the floor price, the system automatically buys back assets from the pool, raising the price above the floor price. The volume of assets to be bought back is determined algorithmically, ensuring a consistent pool price above the floor price. This process is entirely automated and transparent, fostering a stable environment for the KEI token value.

### Reserve Token

KEI token acts as a reserve token, backed by each asset held in the treasury, excluding LP and KEI tokens. If the KEI token's market value falls below the floor price, the assets in the treasury are deployed to buy back and burn the depreciated tokens, reinforcing the floor price.

### Multi-Coin Treasury Backed

The treasury currently holds ETH as its reserve, but is designed to support a range of other assets like BTC and DAI. This multi-coin backing enriches the treasury's capacity to support the KEI token's floor price.

### Floor Price Walkthrough

The floor price is calculated based on the fluctuating prices of each asset in the treasury, primarily valued in ETH. As a result, the KEI token's value is essentially tethered to the value of ETH, meaning that the rise in ETH's value consequently elevates the KEI token's value. The 1:1 ETH-to-KEI ratio simplifies the floor price calculation as long as the treasury only holds ETH.

The floor price influences the minting of new tokens. Each minted token must be backed by an equivalent amount of ETH, ensuring the floor price never declines. Conversely, when a token is burnt or new assets are deposited into the treasury, the floor price rises.

This unique mechanism of KEI Finance not only ensures stability but also promotes a steady growth of the token value, making it an attractive choice for stakeholders.

## Floor Price Calculation

In order to calculate the floor price the following calculation is done:

<table><thead><tr><th width="263">Variable</th><th>Details</th></tr></thead><tbody><tr><td>p</td><td>The resulting floor price</td></tr><tr><td>tokensCirculating</td><td>The total tokens which are not in the liquidity pools. (able to be sold)</td></tr><tr><td>tokenReserves</td><td>The total tokens in the liquidity pools (not able to be sold)</td></tr><tr><td>backingTreasury</td><td>The total value in ETH in the treasury (used for buying back tokens)</td></tr><tr><td>backingReserves</td><td>The total value in ETH in liquidity pools (will be swapped for tokens)</td></tr><tr><td>decimals</td><td>How much decimal precision we want to work with (all solidity math is in ints, so we need to make them decimals).</td></tr></tbody></table>

<figure><img src="../.gitbook/assets/image (10).png" alt=""><figcaption><p>formula for calculating the floor price</p></figcaption></figure>

