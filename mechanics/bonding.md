---
description: Supporting long-term growth through sustainable token supplies.
---

# 🔓 Supplying

{% hint style="info" %}
**The Supplier:** Integrated into the swap router, the supplier contract is responsible for minting daily tokens in direct balance with the current number of protocol users.
{% endhint %}

### Introduction to The Supplier.

The supplier works in sync with the custom Kei Finance swap router that determines the best price for fixed token purchases within the last 12 hours of the Uniswap pool. The supplier contract has the ability to mint daily KEI tokens capped at 33 333.&#x20;

Through the minting process a fee is incurred by the protocol which is then split up and distributed throughout the platform to LP pools and user rewards.&#x20;

### How does The Supplier work?&#x20;

The Supplier contract is self-executing, minting 'x' tokens per day where the value of 'x' is determined by the number of staked wallets on that day. Automatic snap shots are taken by the supplier contract to determine number of staked wallets, which then triggers automated KEI token minting.\
\
**Formula:**

(IS IT POSSIBLE TO HAVE A DIAGRAM HERE)&#x20;
