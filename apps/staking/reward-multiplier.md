---
description: The multiplier applied to your stake, increasing the return on your rewards.
---

# Reward Multiplier

{% hint style="info" %}
The **Reward Multiplier** is based on how long you decide to stake for. The longer you stake, the higher multiplier, and in return higher rewards.
{% endhint %}

### Current Rates

| Property           | Value |
| ------------------ | ----- |
| Min Stake Duration | 0     |
| Max Stake Duration | 3333  |
| Min Multiplier     | 1     |
| Max Multiplier     | 100   |

{% embed url="https://infogram.com/reward-multiplier-1hd12yx7nn0jx6k?live=" %}

### Formula

The formula associated with what multiplier you receive is calculated as such:

| Variable | Value                 |
| -------- | --------------------- |
| a        | Min Reward Multiplier |
| b        | Max Reward Multiplier |
| c        | Max Stake Duration    |
| d        | Stake Duration        |
| x        | Reward Multiplier     |

$$
f(x) = a + (d/c)^2 * (b - a)
$$
