---
description: description
---

# NFT Descriptor

## Read Methods

### Create Token Uri

description

```solidity
function createTokenURI(NFTDetails memory stake) external pure returns (string memory uri);
```

## Structs

### Nft Details

description

```solidity
struct NFTDetails {
    uint256 stakeId;
    IStaking.Stake stake;
    uint256 rewards;
    uint256 principal;
    uint256 unstakePenalty;
    uint256 unstakePenaltyPercent;
}
```
