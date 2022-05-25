---
description: description
---

# Token Controller

## Read Methods

### Unlock Role

description

```solidity
function UNLOCK_ROLE() external pure returns (bytes32);
```

### Unlocked

description

```solidity
 function unlocked() external view returns (bool);
```

### Can Transfer

description

```solidity
function canTransfer(address from, address to, uint256 amount) external view returns (bool);
```

## Write Methods

### Unlock

description

```solidity
function unlock() external
```

### Lock

description

```solidity
 function lock() external;
```

### Handle Transfer

description

```solidity
 function handleTransfer(IKEI.Snapshot memory k, address from, address to, uint256 amount) external
```
