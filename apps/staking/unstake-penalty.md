---
description: >-
  The penalty associated with withdrawing your stake before the designated stake
  end date.
---

# Unstake Penalty

{% hint style="warning" %}
It is important to understand the penalties associated with unstaking before the designated stake end date. This is to ensure that you do not have any unexpected losses.
{% endhint %}

### Current Penalty

| Property    |     |
| ----------- | --- |
| Min Penalty | 0   |
| Max Penalty | 100 |

{% embed url="https://infogram.com/unstake-penalty-1h7j4dvy03egv4n?live=" %}

### Formula

The formula associated with what penalty you receive is calculated as such:

| Variable | Value                      |
| -------- | -------------------------- |
| a        | Min Penalty                |
| b        | Max Penalty                |
| c        | Current Stake Duration (%) |
| x        | Unstake Penalty (%)        |

$$
f(x) = b - (c^2 * (b - a))
$$

