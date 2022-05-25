---
description: description
---

# Fees

## Read Methods

### Manage Role

description

```solidity
 function MANAGE_ROLE() external view returns (bytes32);
```

### Recieve Fee For&#x20;

description

```solidity
function receiveFeeFor(address targetAddress) external view returns (uint256);
```

### Send Fee For

description

```solidity
 function sendFeeFor(address targetAddress) external view returns (uint256);
```

## Write Methods

### Set Fees For

description

```solidity
function setFeesFor(address target, uint256 newReceiveFee, uint256 newSendFee) external;
```

### Exclude From Fee

description

```solidity
function excludeFromFee(address targetAddress) external;
```

### Include In Fee

description

```solidity
function includeInFee(address targetAddress) external;
```

### Exclude From Fee

description

```solidity
function excludedFromFee(address account) external view returns (bool);
```

### Get Transfer Fee

description

```solidity
function
getTransferFee(
IKEI.Snapshot memory k,
address from,
address to,
uint256 amount
) external view returns (uint256 totalFee);
```

## Events

### Fees Updated

description

```solidity
event FeesUpdated(address indexed target,uint256 prevReceiveFee, uint256 prevSendFee, uint256 newReceiveFee, uint256 newSendFee);
```
