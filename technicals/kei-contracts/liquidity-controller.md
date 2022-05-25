---
description: description
---

# Liquidity Controller

## Read Methods

### Manage Role

description

```solidity
function MANAGE_ROLE() external pure returns (bytes32);
```

### Admin Role

description

```solidity
 function ADMIN_ROLE() external pure returns (bytes32);
```

### Lock Duration

description

```solidity
function LOCK_DURATION() external pure returns (uint256);
```

### Max K Value

description

```solidity
function maxKValue(address asset) external view returns (uint256);
```

### Reward Asset

description

```solidity
function rewardAsset() external view returns (address);
```

### Discount

description

```solidity
function discount() external view returns (uint256);
```

## Write Methods

### Set Reward Asset

description

```solidity
 function setRewardAsset(address asset) external;
```

### Set Max K Value

description

```solidity
function setMaxKValue(address asset, uint256 maxK) external;
```

### Set Discount

description

```solidity
function setDiscount(uint256 _discount) external;
```

### Supply Liquidity

description

```solidity
function supplyLiquidity(
    IKEI.Snapshot memory k,
    address asset,
    uint256 assetAmount,
    uint256 stakingDuration
) external;
```

### Mint Liquidity

description

```solidity
function mintLiquidity(address asset, uint256 assetAmount) external;
```

### Burn Liquidity

description

```solidity
function burnLiquidity(address asset, uint256 lpAmount) external;
```

### Process

description

```solidity
function process(IKEI.Snapshot memory k) external;
```

## Events&#x20;

### Reward Asset Updated

description

```solidity
event RewardAssetUpdated(address indexed prevAsset, address indexed newAsset, address indexed sender);
```

### Max K Value Updated&#x20;

description

```solidity
event MaxKValueUpdated(address indexed asset, uint256 prevKValue, uint256 newKValue, address indexed sender);
```

### Discount Updated

description

```solidity
event DiscountUpdated(uint256 prevDiscount, uint256 newDiscount, address indexed sender);
```

### Liquidity Supplied

description

```solidity
event LiquiditySupplied(
    address indexed asset,
    uint256 assetAmount,
    uint256 tokenAmount,
    uint256 indexed stakeId,
    address indexed sender
);
```
