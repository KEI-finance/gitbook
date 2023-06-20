---
description: The core admin contract which receives the admin rewards from the protocol.
---

# Admin

{% hint style="info" %}
A percentage of rewards are distributed to the admin contract to assist with development, marketing and growth of the protocol.
{% endhint %}

> Admin reward percent: **10%**
>
> A percentage of these rewards are allocated to [Affiliate](../../kei-financial-services/affiliate/) rewards.

TODO burn affiliate leftover funds

## Read Methods

### Admin Role

Description

```solidity
function ADMIN_ROLE() external view returns (bytes32);
```

### Admin Withdraw Role

Description

```solidity
function ADMIN_WITHDRAW_ROLE() external view returns (bytes32);
```

## Write Methods

### Withdraw

Description

```solidity
function withdraw(address to, uint256 totalRewards) external;
```
