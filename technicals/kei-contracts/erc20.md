---
description: description
---

# ERC20

## Read Methods

### Total Supply

description

```solidity
function totalSupply() external view returns (uint256);
```

### Balance Of

description

```solidity
function balanceOf(address account) external view returns (uint256);
```

### Allowance

description

```solidity
function allowance(address owner, address spender) external view returns (uint256);
```

## Write Methods

### Transfer

description

```solidity
 function transfer(address to, uint256 amount) external returns (bool);
```

### Approve

description

```solidity
function approve(address spender, uint256 amount) external returns (bool);
```

### Transfer From

description

```solidity
function transferFrom(
    address from,
    address to,
    uint256 amount
) external returns (bool);
```

## Events

### Transfer

description

```solidity
 event Transfer(address indexed from, address indexed to, uint256 value);
```

### Approval

description

```solidity
 event Approval(address indexed owner, address indexed spender, uint256 value);
```
