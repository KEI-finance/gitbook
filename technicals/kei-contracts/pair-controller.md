---
description: description
---

# Pair Controller

## Read Methods

### Pair To Asset

description

```solidity
function pairToAsset(address pair) external view returns (address asset);
```

### Asset To Pair

description

```solidity
 function assetToPair(address asset) external view returns (address pair);
```

### Is Controlled Pair

description

```solidity
 function isControlledPair(address pair) external view returns (bool);
```

### Total Controlled Pairs

description

```solidity
 function totalControlledPairs() external view returns (uint256);
```

### Controlled Pair

description&#x20;

```solidity
function controlledPair(uint256 i) external view returns (IUniswapV2Pair);
```

### Controlled Pairs

description

```solidity
 function controlledPairs() external view returns (address[] memory pairs);
```

## Write Methods

### Initialize

description

```solidity
function initialize(
    IKEI.Snapshot memory k,
    address asset,
    uint256 tokenAmount,
    uint256 backingAmount
) external;
```

### Pre Sync

description

```solidity
 function preSync(IKEI.Snapshot memory k, address pairAddress) external returns (IPricing.Prices memory);
```

### Post Sync

description

```solidity
function postSync(IKEI.Snapshot memory k, address pairAddress) external returns (IPricing.Prices memory);
```

### Sync

description

```solidity
 function sync(IKEI.Snapshot memory k, address asset) external returns (IPricing.Prices memory);
```

## Structs

### Reserve Details

description

```solidity
struct ReserveDetails {
    bool tokenIs0;
    address pair;
    address asset;
    uint112 assetReserves;
    uint112 tokenReserves;
    uint256 assetReservesBASE;
}
```
