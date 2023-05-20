---
description: Understand how the KEI token increases the protocol's floor price
---

# 📈 Floor Price

## Floor Price Mechanism

KEI Finance utilizes a unique and groundbreaking "Raising Floor Price" mechanism, distinguishing it from other DeFi protocols and promoting the stability and growth of the KEI token's value. This innovative method creates a floor price - a minimum value that the KEI token cannot fall below, maintained by a continuous automated buyback and burn process.

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

Diagram:

```mathematica
                                 KEI Finance Floor Price Mechanism
                                             ___________________
                                            |                   |
                                            |      Treasury     |
                                            |   (ETH, BTC, DAI) |
                                            |___________________|
                                                  /          \
                                                 /            \
                                                /              \
                                    _________ /                \ _________
                                   |                           |         |
                                   |     Buyback Mechanism     |  Reserve Token
                                   |    (Automated & Transparent) |   (Backed by Treasury Assets)
                                   |___________________________|         |
                                                  |                      |
                                                  |                      |
                                        _________|_________             |
                                       |                   |            |
                                       |      Pool Price   |            |
                                       |   (Maintained Above Floor Price) |
                                       |___________________|            |
                                                  |                      |
                                                  |                      |
                                  _________ ______|_______ _______      |
                                 |         |               |       |     |
                                 |   Buy   |   Sell Transactions   |  Burn
                                 |_________|_______________|_______|     |
                                                  |                      |
                                                  |                      |
                                        _________|_________       _______|_______
                                       |                   |     |               |
                                       |      Floor Price  |     |  KEI Token Value
                                       |(Influences Minting & Burning) | (Stable & Growing)
                                       |___________________|     |_______________|
```

This floor price mechanism safeguards KEI's token value while fostering growth,
