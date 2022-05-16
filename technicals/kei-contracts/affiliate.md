---
description: description
---

# Affiliate

## Read methods

### Get Id

description

```solidity
function getId(address affiliate) external view returns (bytes32);
```

### Get Affliate

description

```solidity
function getAffiliate(bytes32 id) external view returns (address);
```

### Get Referrer

description

```solidity
function getReferrer(address account) external view returns (address);
```

### Balance Of

description

```solidity
function balanceOf(address account) external view returns (uint256);
```

### Has Been Assigned

description

```solidity
function hasBeenAssigned(address account) external view returns (bool);
```

### Ratio

description

```solidity
function ratio(uint256 index) external view returns (uint256);
```

### Total Ratio&#x20;

description

```solidity
function totalRatio() external view returns (uint256);
```

### Ratios&#x20;

description

```solidity
function ratios() external view returns (uint256[] memory);
```

## Write Methods

### Set Id

description

```solidity
function setID(bytes32 id) external;
```

### Assign To&#x20;

description

```solidity
function assignTo(bytes32 id) external;
```

### Withdraw

description

```solidity
function withdraw(address to, uint256 amount) external;
```

### Reward

description

```solidity
function reward(uint256 totalTokens, address sender) external returns (uint256 remainder);
```

## Events

### Withdrawal

Description

```solidity
event Withdrawal(
    address indexed to, 
    uint256 amount, 
    address indexed sender
);
```

### ID Updated

Description

```solidity
event IDUpdated(
    bytes32 indexed prevId, 
    bytes32 indexed newId,
    address indexed sender
); 
```

##
