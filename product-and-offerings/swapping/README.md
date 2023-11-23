---
description: Advanced Swapping, Simplified
cover: ../../.gitbook/assets/whitepaper-header.png
coverY: 0
---

# Token Swaps

{% hint style="info" %}
KEI token swaps operate on a Fixed Rate Price model, ensuring that users receive the most advantageous rate when making their purchases directly through our website.
{% endhint %}

Swapping is a Web3 term that means to exchange one token for another token. For example a user can swap their Bitcoin (BTC) for KEI tokens, like swapping 5 euros for 5.5 US dollars.&#x20;

Staking refers to the act of locking your tokens in smart contracts that are like bank vaults where users can earn an interest known as APR on the value of tokens locked in these contracts.&#x20;

Supplier: A contract (Code) specific to the KEI finance protocol that manages the minting of KEI tokens.&#x20;

The swap features offer a seamless onboarding experience onto the KEI Protocol, enabling users to effortlessly stake and swap tokens in a single transaction. By combining these functionalities, it not only saves users on transaction fees but also facilitates a controlled supply flow within the protocol. This innovative mechanism ensures a gradual and stable increase in the token supply while maintaining efficient operations.

Where a swap purchase transaction would look like the following:

<figure><img src="../../.gitbook/assets/image (16).png" alt=""><figcaption></figcaption></figure>

## Supply Percentage: Rewarding Long Term Stakers&#x20;

Swaps employ a user first approach, offering to supplement a percentage of an individual's purchase on their staking duration. This strategy is crafted to deliver higher discounts for more extended staking periods, thereby motivating users to stake longer and receive larger discounts.

Example: If you were to stake your KEI tokens for 12 months you would receive better discounts than someone opting to stake for 6 months.&#x20;

The precise contribution from a swap is not random, but is carefully calculated. It depends on a specific formula that considers the length of staking among other factors. The formula is as follows:

| Variable |                                     |
| -------- | ----------------------------------- |
| x        | Percentage that will be supplied    |
| P        | The maximum supply percentage       |
| p        | The minimum supply percentage       |
| S        | The maximum stake duration          |
| s        | The minimum stake duration          |
| t        | The users designated stake duration |

<figure><img src="../../.gitbook/assets/image (17).png" alt="" width="375"><figcaption><p>Formula to calculate supply percent</p></figcaption></figure>

| Maximum Stake Duration    | 3333 Days |
| ------------------------- | --------- |
| Minimum Stake Duration    | 0 Days    |
| Maximum Supply Percentage | 80%       |
| Minimum Supply Percentage | 3%        |

## Fixed Rate Price: Competitive Token Prices

The Fixed Rate Price represents the established cost at which each token is sold during its distribution phase through the supplier. It provides a contrast to the Automated Market Maker (AMM) model, where every subsequent token purchased incrementally escalates the token's price. To make this proposition more attractive, a special discount is applied to the fixed rate, designed to encourage purchases directly through our website, and to incentivize long-term token holdings.

Determining the specific fixed rate for a particular token is a straightforward process. It can be derived using the following formula:

<table><thead><tr><th width="192">Variable</th><th>Meaning</th></tr></thead><tbody><tr><td>x</td><td>The price of the of the fixed rate supplied tokens</td></tr><tr><td>d</td><td>The discount applied in percent (example: 0.2 for 20%)</td></tr><tr><td>p</td><td>The current price of the token in based on the supply</td></tr></tbody></table>

<figure><img src="../../.gitbook/assets/image (8).png" alt="" width="274"><figcaption><p>Formula to calculate fixed rate price</p></figcaption></figure>

| Discount Rate | 20% |
| ------------- | --- |

## Distribution of Funds: Benefitting All Investors

When the supplier springs into action and new tokens are minted, the funds received from the purchase are divided into two key portions. The first segment directly supports each minted token, establishing its inherent value. The remainder of the funds is seen as profit.

The focus of these profit mechanics is twofold:&#x20;

1\) Foster the protocol's growth and bolstering the liquidity pool. The expansion of the liquidity pool contributes to price stability, preventing sharp fluctuations and ensuring a smoother trading experience.

2\) The profit tokens add growth to the protocol and value for all investors by raising the floor price and providing attractive staking rewards.

The following diagram provides a clear illustration of how the funds are initially distributed upon supply:

<figure><img src="../../.gitbook/assets/image (22).png" alt=""><figcaption><p>Distribution Diagram</p></figcaption></figure>

{% hint style="info" %}
This method allows the liquidity pool to expand autonomously through the protocol's automation, eliminating the need for manual user input.
{% endhint %}

## Transaction Fees: Fuelling the Protocol

Every transaction incurs a fee that fuels the protocol's growth, benefitting all investors within the protocol. The prevailing fee structure is as follows:

<table data-header-hidden><thead><tr><th>Type</th><th>Amount</th><th data-hidden></th></tr></thead><tbody><tr><td>Buying</td><td>0.6%</td><td></td></tr><tr><td>Selling</td><td>0.6%</td><td></td></tr></tbody></table>

When purchases are made directly through the website, the buy fee is effectively mitigated by the application of a discounted supply rate. This mechanism implies the potential for a fee-free purchase experience on the website, as the applied discount could entirely offset the buying fee.

