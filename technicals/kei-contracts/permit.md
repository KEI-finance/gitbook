---
description: description
---

# Permit

## Read Methods

### Nonces

description

```solidity
function nonces(address owner) external view returns (uint256);
```

### Domain Seperator

description

```solidity
function DOMAIN_SEPARATOR() external view returns (bytes32);
```

## Write Methods

### Permit

description

```solidity
function permit(
address owner,
address operator,
uint256 deadline,
uint8 v,
bytes32 r,
bytes32 s
) external;
```
