---
description: description
---

# Treasury

## Read Methods

### Balance Of

description

```solidity
function balanceOf(address asset) external view returns (uint256);
```

### Reserves

description

```solidity
 function reserves(address asset) external view returns (uint256);
```

### Role Of

description

```solidity
 function roleOf(address asset) external pure returns (bytes32);
```

## Write Methods

### Withdraw

description

```solidity
function withdraw(address asset, address to, uint256 amount) external;
```

### Sync

description

```solidity
  function sync(address asset) external returns (uint256 received);
```

## Events

### Asset Withdrawn

description

```solidity
 event AssetWithdrawn(address indexed asset, address indexed to, uint256 amount, address indexed sender);
```

### Asset Deposited

description

```solidity
event AssetDeposited(address indexed asset, uint256 amount, address indexed sender);
```
