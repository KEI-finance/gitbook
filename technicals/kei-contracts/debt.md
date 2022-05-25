---
description: description
---

# Debt

## Read Methods

### Debt Of&#x20;

description

```solidity
function debtOf(address asset) external view returns (uint256);
```

### Total Debt Assets

description

```solidity
function totalDebtAssets() external view returns (uint256);
```

### Debt Asset&#x20;

description

```solidity
function debtAsset(uint256 index) external view returns (address);
```

## Write Methods

### Register Debt

description

```solidity
function registerDebt(address asset, uint256 amount) external;
```

### Register Payment

description

```solidity
function registerRepayment(address asset, uint256 amount) external returns (uint256 amountPaid, uint256 overflowed);
```

### Borrow&#x20;

description

```solidity
 function borrow(IKEI.Snapshot memory k, address asset, address to, uint256 amount) external;
```

### Repay

description

```solidity
 function repay(IKEI.Snapshot memory k, address asset) external returns (uint256 amountPaid, uint256 overflowed);
```

### Process&#x20;

description

```solidity
function process(IKEI.Snapshot memory k) external;
```

## Events

### Debt Repay Fees

description

```solidity
 event DebtRepaid(address indexed asset, uint256 totalAmount, uint256 debtReduction, uint256 overflowAmount, address indexed sender);
```

### Debt Created

description

```solidity
event DebtCreated(address indexed asset, uint256 amount, address indexed sender);
```
