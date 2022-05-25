---
description: description
---

# Bonding

## Read methods

### Config

description

```solidity
function config(address asset) external view returns (AssetConfig memory);
```

### Allowance Interval

description

```solidity
function allowanceInterval() external view returns (uint256);
```

### Bond Price Time Stamp Delay

description

```solidity
function bondPriceTimestampDelay() external view returns (uint256);
```

### Interval Start At&#x20;

description

```solidity
function intervalStartAt() external view returns (uint256);
```

### Is Enabled

description

```solidity
function isEnabled(address asset) external view returns (bool);
```

### Enabled&#x20;

description

```solidity
function enabled() external view returns (address[] memory);
```

### Estimate Token Amount

description

```solidity
function estimateTokenAmount(IKEI.Snapshot memory k, address asset, uint256 assetAmount) external view returns (uint256);
```

### Current Bond Interval

description

```solidity
function currentBondInterval() external view returns (uint256);
```

### Current Interval Token Bonded

description

```solidity
function currentIntervalTokensBonded(address asset) external view returns (uint256);
```

### Remaining Bond Allowance

description

```solidity
function remainingBondAllowance(address asset) external view returns (uint256);
```

### Bond Price

description

```solidity
function bondPrice(
    IKEI.Snapshot memory k,
    uint256 floorPrice,
    address asset
) external view returns (uint256);
```

## Write Methods

### Approve

description

```solidity
function approve() external;
```

### Enable

description

```solidity
function enable(address asset) external;
```

### Disable&#x20;

description

```solidity
function disable(address asset) external;
```

### Update Config

description

```solidity
function updateConfig(address asset, AssetConfig memory config) external;
```

### Bond

description

```solidity
function bond(
    IKEI.Snapshot memory k,
    address asset,
    uint256 assetAmount,
    uint256 stakingDuration
) external returns (BondDetails memory);
```

## Events

### Bonds created

description

```solidity
event BondCreated(BondDetails details, address indexed sender);
```

### Asset Config Update

description

```solidity
event AssetConfigUpdated(AssetConfig prevConfig, AssetConfig newConfig, address indexed sender);
```

## Structs

### Asset Config

description

```solidity
struct AssetConfig {
    uint256 allowance;
    uint256 lockDuration;
    uint256 discountPercent;
    uint256 baseIncrementPercent;
}
```

### Bond Details&#x20;

description

```solidity
struct BondDetails {
    address asset;
    uint256 assetAmount;
    uint256 assetReceived;
    uint256 assetReceivedBASE;
    uint256 tokensAllocated;
    uint256 bondPrice;
    uint256 stakeId;
}
```

###

