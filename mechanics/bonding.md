---
description: Supporting long-term growth through sustainable token supplies.
cover: ../.gitbook/assets/Screen Shot 2023-05-25 at 10.46.33.png
coverY: 0
---

# 🔓 Supplying

{% hint style="info" %}


**The Supplier:** Integrated into the swap router, the supplier contract is responsible for minting daily tokens in direct balance with the current number of protocol users.
{% endhint %}

### <mark style="color:purple;">Introduction to The Supplier.</mark>

The supplier works in sync with the custom Kei Finance swap router that determines the best price for fixed token purchases within the last 12 hours of the Uniswap pool. The supplier contract has the ability to mint daily KEI tokens capped at <mark style="background-color:green;">33 333</mark>.&#x20;

Through the minting process a fee is incurred by the protocol which is then split up and distributed throughout the platform to LP pools and user rewards.\
\
<mark style="color:purple;">**Example:**</mark> If the supplier mints $10 worth of KEI the 3% fee is applied distributing $0.30 to the platform.

### <mark style="color:purple;">How does The Supplier work?</mark>&#x20;

The Supplier contract is self-executing, minting 'x' tokens per day where the value of 'x' is determined by the number of staked wallets on that day. Automatic snap shots are taken by the supplier contract to determine number of staked wallets, which then triggers automated KEI token minting.

<mark style="background-color:green;">Kevin please break this page down further</mark>\
\
**Formula:**

(<mark style="background-color:green;">IS IT POSSIBLE TO HAVE A DIAGRAM HERE)</mark>&#x20;
