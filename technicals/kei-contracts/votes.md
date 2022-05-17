---
description: description
---

# Votes

## Read Methods

### Total Supply

description

```solidity
function totalSupply() external view returns (uint256);
```

### Total Holders

description

```solidity
function totalHolders() external view returns (uint256);
```

### Balance Of

description

```solidity
function balanceOf(address account) external view returns (uint256);
```

### Get Past Total Holders

description

```solidity
 function getPastTotalHolders(uint256 blockNumber) external view returns (uint256);
```

## Events&#x20;

### Total Holders Changed

description

```solidity
event TotalHoldersChanged(uint256 prevTotalHolders, uint256 newTotalHolders);
```
