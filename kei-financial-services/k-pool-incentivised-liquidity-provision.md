---
cover: ../.gitbook/assets/Screen Shot 2023-05-25 at 10.46.33.png
coverY: 0
---

# 🎲 K-Pool: Incentivised Liquidity Provision

<mark style="background-color:green;">Need to confirm all this with Kevin / conceptualise how it works with LP pool</mark>

### <mark style="color:purple;">Weekly Gamified Liquidity Incentives</mark>&#x20;

To encourage users to provide liquidity to the KEI LPs, Kei Finance incorporates a unique No Loss weekly token draw. Users who supply KEI as a form of liquidity can enter the Weekly Token Games. Users receive a number of tickets that represent their stake in the liquidity pool. At the end of each week a random wallet is selected via on-chain mappable data and the winning amount of tokens is transferred to their wallet.&#x20;

### <mark style="color:purple;">Timed Ticket Value Distribution</mark>&#x20;

In order to stop large Liquidity Providers from entering the weekly games at the end of a cycle and boosting their chances of winning, a time-based ticket allocation mechanic has been integrated. This ticket allocation-holding is based on the amount of KEI supplied and which day of the games you supplied.\
\
<mark style="color:purple;">**Example:**</mark> \
User A supplies 100 KEI tokens on day 1 of the weekly games. Each 1 KEI on day 1 provides 1000 tickets. User A receives 100 000 tickets _(100KEIx1000 tickets per KEI)._ \
\
User B supplies 100 000 KEI tokens on day 7 of the weekly games one hour before the selection. Each 1 KEI on day 7 provides 1 ticket. User B receives 100 000 tickets. _(100 000KEIx 1 ticket per KEI)_&#x20;

<mark style="color:purple;">**Formula:**</mark>** 1)** z = ((1 - ((168 - t) / 168)) \* (100000 - 1)) + 1 **2)** x = z \* y\
\
x = be the amount of tickets received.

y = be the amount of tokens deposited in the pool.

z = be the ticket allocation determined by tokens deposited and time of deposit.

t = represents the time of deposit in hours, ranging from 0 to 168.

### <mark style="color:purple;">Winning Token Distribution</mark>&#x20;

The tokens allocated as winnings for the selected wallet is calculated based on the current state of the liquidity pool at time of selection. A snapshot is conducted at the moment of selection to determine the current value in tokens of the liquidity pool, the number of liquidity providers and the percentage share of the pool for each provider. Using this information the smart contract calculates the token amount distributed as winnings to the selected wallet. \
\
<mark style="color:purple;">**Formula:**</mark> X = (y / 100) \* z

_Winnings = x_&#x20;

_% share of LP = y_&#x20;

_Number of providers = z_&#x20;

_Reward pool = v_ \


