---
description: Staking and their NFT's
---

# Staking NFT's

{% hint style="success" %}
Every stake created, also creates a NFT which represents the stakes position.&#x20;
{% endhint %}

The staking contract is actually an [ERC1155](nft-stake.md#erc1155) rather than an [ERC20](https://eips.ethereum.org/EIPS/eip-20). Which means that every stake created is treated as an NFT and thus, can be sold on NFT marketplaces supporting this token standard.&#x20;

This standard introduces a total supply for each NFT, meaning that each stake also comes with a total supply. This supply is minted to the account which that stake is for, and can thus be transfer from account to account, partially or entirely.

Anyone who owns a portion of your stake is able to unstake it at anytime, taking from a portion of the total pool. To find out more about the calculations and how this works, visit [Staking Calculations](staking-calculations.md).

## Designs

### Basic Design (1x)

{% embed url="https://assets.kei.fi/nft-basic.svg" %}

### Medium Design (50x)http

{% embed url="https://assets.kei.fi/nft-medium.svg" %}

### Rare Design (100x)

{% embed url="https://assets.kei.fi/nft-rare.svg" %}

## ERC1155

{% embed url="https://eips.ethereum.org/EIPS/eip-1155" %}
Read more about the specific standard
{% endembed %}
