---
description: 'Protocol Staking: Amplifying Investment Growth Through Commitment'
cover: ../.gitbook/assets/whitepaper-header.png
coverY: 0
---

# K-Stake

{% hint style="info" %}
The staking platform on Kei Finance transcends the mere role of offering rewards to investors in the protocol. It also stands as the principal interface for engaging with the protocol. Coupled with reward multipliers, it amplifies your user experience and return on investment, making it more than just a passive investment platform.
{% endhint %}

<figure><img src="../.gitbook/assets/image (33).png" alt=""><figcaption><p>KEI Staked Positions. (Note: days are only visual and do not accurately reflect multiplier).</p></figcaption></figure>

## **The Core Function: Long-Term Capital Growth**

The staking function within Kei Finance plays an essential role in fostering long-term investment growth. By staking KEI tokens, users participate in the protocol's continuous operability, securing and nurturing their investments. The overarching philosophy of KEI staking is straightforward - the longer the stake, the higher the rewards.

## **Reward Redistribution: Recirculating Value**

A percentage of all rewards generated by the platform's operations are redistributed directly to stakers. This continuous reallocation of earnings not only amplifies staker returns but also promotes long-term commitment to the protocol.

<figure><img src="../.gitbook/assets/image (32).png" alt=""><figcaption><p>Profits from each tool, going back to Stakers.</p></figcaption></figure>

## **Staked-KEI Tokens: The Staking Commitment**

Users stake their KEI tokens for a predefined duration to earn staked-KEI tokens (sKEI). These tokens represent a user's stake position and commitment to the protocol. Unstaking sKEI before the end of the predetermined staking period will invoke a penalty, reinforcing the principle of responsible staking.

### Reward Multiplier: Increasing ROI

The longer you keep your money staked, the more rewards you can get. These extra rewards apply across all parts of the Kei Protocol, helping you earn more from every tool and service. For example, if you have a 10x reward multiplier, you could get about 10 times more rewards than someone with a 1x multiplier.

<figure><img src="../.gitbook/assets/image (15).png" alt=""><figcaption></figcaption></figure>

### Calculating the Reward Multiplier

<table><thead><tr><th width="219">Variable</th><th>Meaning</th></tr></thead><tbody><tr><td>r</td><td>The resulting reward multiplier</td></tr><tr><td>ks</td><td>The kink stake duration position</td></tr><tr><td>km</td><td>The kink reward multiplier position </td></tr><tr><td>m</td><td>The min reward multiplier</td></tr><tr><td>M</td><td>The max reward multiplier</td></tr><tr><td>s</td><td>The min staking duration</td></tr><tr><td>S</td><td>The max staking duration</td></tr><tr><td>x</td><td>The user input staking duration</td></tr></tbody></table>

<figure><img src="../.gitbook/assets/image (35) (1).png" alt="" width="563"><figcaption><p>Calculation for Reward Multiplier</p></figcaption></figure>

## **Penalty Structure: Discouraging Early Unstaking**

The penalty incurred for early unstaking is calculated based on the fraction of the committed staking period completed. The longer the staking duration and the earlier the unstaking, the higher the penalty imposed. This model encourages users to fully honor their staking commitments to maximize their rewards.

This deterrent discourages impulsive entry and exit from the staking pool, fostering a more stable and dependable staking environment.

> **Unstaking Penalty Example:** _A user staking their KEI tokens for a year who decides to unstake within the first 10 days could incur a penalty as high as 99% of the stake. In contrast, a user opting to unstake on the 340th day could incur a significantly lower penalty, reflecting the completed duration of their staking commitment._

<figure><img src="../.gitbook/assets/image (31).png" alt=""><figcaption></figcaption></figure>

### Calculating the Unstake Penalty

<table><thead><tr><th width="219">Variable</th><th>Meaning</th></tr></thead><tbody><tr><td>u</td><td>The resulting penalty</td></tr><tr><td>kd</td><td>The kink duration position</td></tr><tr><td>kp</td><td>The kink penalty position </td></tr><tr><td>p</td><td>The min penalty</td></tr><tr><td>P</td><td>The max penalty</td></tr><tr><td>d</td><td>The committed stake duration</td></tr><tr><td>x</td><td>The current days that have passed</td></tr></tbody></table>

<figure><img src="../.gitbook/assets/image.png" alt="" width="563"><figcaption></figcaption></figure>

## **Penalties and Principal: A Responsible Balance**

Initially, the penalties are applied to the staking profits. However, premature unstaking could result in penalties being deducted from the staked principal. The precise impact depends on how early a user decides to unstake.

## **Partial Unstaking: Offering Flexibility**

Recognizing the need for flexibility, KEI Finance allows stakers to partially unstake their tokens, incurring penalties only on the unstaked portion at that specific time. This feature provides stakers with an added layer of control over their investment strategy.

## Auto-Compounding x Reward Multiplier: Maximising ROI

The staking algorithm utilized by the Kei Protocol is pioneering in its integration of both auto-compounding and reward multiplier mechanics within a single staking pool. This unique structure endows users with the assurance of long-term staking without the risk of stake dilution as new participants enter the pool. Simultaneously, it empowers users to accrue higher rewards, even with a lower stake commitment, thereby optimizing their investment potential.

## Trading Staked Positions: Avoid fees for greater flexibility&#x20;

Furthering the recognition of flexibility, users also have the option to sell their whole of partial position to other users who take on the staking period committment. Learn more of trading staked positions in the [K-Positions](k-positions-coming-soon/) section.&#x20;

## **Post-Duration Rewards: No Penalties, Continuous Earnings**

Once the committed staking duration is over, stakers continue earning rewards on their staked KEI tokens until they decide to unstake. At this stage, unstaking can be executed at any time without incurring any penalties, rewarding stakers for their completed commitment.