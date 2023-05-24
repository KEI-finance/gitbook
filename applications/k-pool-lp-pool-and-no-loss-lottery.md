---
description: >-
  Provide liquidity to strengthen the Kei Finance platform and go into the draw
  to receive weekly KEI payouts for selected wallets.
---

# 🎲 K-Pool: LP Pool & No-loss token games

### Weekly Token Games: Gamified Liquidity Incentives&#x20;

To encourage users to provide liquidity to the KEI LPs, Kei Finance incorporates a unique No Loss Token Game. Users who supply KEI as a form of liquidity will automatically enter the Weekly Token Games. Users receive a number of tickets that represent their stake in the liquidity pool. At the end of each week a random wallet is selected via on-chain mappable data and the winning amount of tokens is transferred to their wallet.&#x20;

### Timed Ticket Value Distribution&#x20;

In order to stop large token holding wallets from entering the weekly games at the end of a cycle and boosting their chances of winning, a time based ticket allocation mechanic has been integrated. This ticket allocation is based on not only the amount of KEI supplied but also on which day of the games you supplied. \
\
**Example:** \
User A supplies 100 KEI tokens on day 1 of the weekly games. Each 1 KEI on day 1 provides 1000 tickets. User A receives 100 000 tickets _(100KEIx1000 tickets per KEI)._ \
\
User B supplies 100 000 KEI tokens on day 7 of the weekly games one hour before the selection. Each 1 KEI on day 7 provides 1 ticket. User B receives 100 000 tickets. _(100 000KEIx 1 ticket per KEI)_&#x20;

**Formula: 1)** z = ((1 - ((168 - t) / 168)) \* (100000 - 1)) + 1 **2)** x = z \* y\
\
x = be the amount of tickets received.

y = be the amount of tokens deposited in the pool.

z = be the ticket allocation determined by tokens deposited and time of deposit.

t = represents the time of deposit in hours, ranging from 0 to 168.

### Winning Token Distribution&#x20;

The tokens allocated as winnings for the selected wallet is calculated based on the current state of the liquidity pool at time of selection. A snapshot is conducted at the moment of selection to determine the current value in tokens of the liquidity pool, the number of liquidity providers and the percentage share of the pool for each provider. Using this information the smart contract calculates the token amount distributed as winnings to the selected wallet. \
\
**Formula:** X = (y / 100) \* z

_Winnings = x_&#x20;

_% share of LP = y_&#x20;

_Number of providers = z_&#x20;

_Reward pool = v_ \


