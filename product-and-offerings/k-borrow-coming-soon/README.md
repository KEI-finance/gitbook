---
description: Integrating a unique model that empowers secure borrowing practices
cover: ../../.gitbook/assets/whitepaper-header.png
coverY: 0
---

# K-Borrow - Coming Soon

## How it works&#x20;

In Kei Finance, the K-Borrow feature operates using the [Reserve Currency](broken-reference) functionalities. This enables users to utilise their stakes as collateral to borrow from the treasury reserve assets. The unique aspect of this setup is that there is no requirement for a separate lender, as the protocol itself acts as the lender. As a result, all lending profits are directed back to the protocol, benefiting KEI holders and KEI stakers through rewards and incentives. This approach ensures that the protocol remains self-sustaining and supports the community of token holders and stakers.

<figure><img src="../../.gitbook/assets/image (39).png" alt=""><figcaption><p>K-Borrow</p></figcaption></figure>

> **Example:** _If the current price of KEI is 0.05 and the floor price is 0.02 the maximum percentage to borrow is 20% of their staked balance._

When a user initiates their loan from the platform their stake which acts as the collateral needed is transferred to a seperate escrow contract. The users stake will remain in the escrow contract until the user decides to pay off the loan and withdraw their staked position.&#x20;

## Borrowing Loopbacks: Maximising growth potential.&#x20;

Users can purchase KEI and borrow ETH. Then use their borrowed ETH to purchase more KEI and stake their newly purchased KEI back into the protocol. A user can continue this loop until the the borrow potential becomes too small to generate significant value. This mechanic enables enhanced and stable borrowed staking rewards.&#x20;

<figure><img src="../../.gitbook/assets/image (29).png" alt=""><figcaption><p>Loopback cycle</p></figcaption></figure>

## Interest Distribution: Secures the treasury and platform liquidity.

100% of the interest paid is protocol profit. This profit is distributed back to the treasury and liquidity pools in order to reinforce a stable treasury and adequate protocol liquidity.  &#x20;

## Debt&#x20;

Debt primarily wraps around the treasury, allowing for controlled asset removal and tracking. This capability ensures stable price maintenance despite asset usage. The eventual introduction of the borrowing functionality will leverage this aspect. The inherent risk in reusing assets in this manner necessitates a cap on accrued debt, set as a percentage of the total treasury balance.

The borrowing contract assures safe token borrowing due to the protocol removing tokens from the market, effectively making it safe to lend up to the token's stable price without algorithmic consequences.

## What happens when a user defaults on their loan?&#x20;

**Option 1:** When a Kei Finance user defaults on their loan other users have the ability to pay the loan off and claim the users staked token position.&#x20;

**Option 2:** Assuming no users have purchased the default loan position the platform can unstake the allocated tokens and burn them. This enables the protocol to claimback the collateral. As the tokens have not exceeded the floor price, there is no loss to the protocol.
