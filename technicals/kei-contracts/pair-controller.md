---
description: description
---

# Pair Controller

## Read Methods

### Manage Role

description

```solidity
 function MANAGE_ROLE() external pure returns (bytes32);
```

### Mint Role&#x20;

description

```solidity
function MINT_ROLE() external pure returns (bytes32);
```

### Burn Role&#x20;

description

```solidity
 function BURN_ROLE() external pure returns (bytes32);
```

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

### Desired K Value

description

```solidity
function desiredKValue(address pair) external view returns (uint256);
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

### Update Desired K Value

description

```solidity
 function updateDesiredKValue(address pair, uint256 kValue) external;
```

### Mint Liquidity

description

```solidity
function mintLiquidity(IKEI.Snapshot memory k, address pair, uint256 assetAmount) external;
```

### Burn Liquidity&#x20;

description

```solidity
 function burnLiquidity(IKEI.Snapshot memory k, address pair, uint256 lpAmount) external;
```

### Create Controlled Pair

description

```solidity
function createControlledPair(IKEI.Snapshot memory k,address asset) external returns (address pair);
```

### Remove Controlled Pair

description

```solidity
 function removeControlledPair(address _pair) external;
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

## Events

### Liquidity Minted

description

```solidity
event LiquidityMinted(
    address indexed asset,
    uint256 assetAmount,
    uint256 tokenAmount,
    uint256 lpAmount,
    address indexed sender
);
```

### Liquidity Burned

description

```solidity
event LiquidityBurned(
    address indexed asset,
    uint256 assetAmount,
    uint256 tokenAmount,
    uint256 lpAmount,
    address indexed sender
);
```

### Controlled Pair Created

description

```solidity
 event ControlledPairCreated(address indexed asset, address indexed pair, address indexed sender);
```

### Controlled Pair Removed

description

```solidity
 event ControlledPairRemoved(address indexed asset, address indexed pair, address indexed sender);
```

### Desired K Value Updated

description

```solidity
event DesiredKValueUpdated(address indexed pair, uint256 prevKValue, uint256 newKValue, address indexed sender);
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
