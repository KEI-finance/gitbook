---
description: description
---

# Pricing

## Read Methods

### Manage Role

description

```solidity
function MANAGE_ROLE() external view returns (bytes32);
```

### Router

description

```solidity
function ROUTER() external view returns (IUniswapV2Router02);
```

### Factory&#x20;

description

```solidity
function FACTORY() external view returns (address);
```

### Base Asset

description

```solidity
function BASE_ASSET() external view returns (address);
```

### Ceiling Percent

description

```solidity
function ceilingPercent() external view returns (uint256);
```

### Evaluated Assets

description

```solidity
function evaluatedAssets(uint256 index) external view returns (address);
```

### Path From Base&#x20;

description

```solidity
function pathFromBase(address asset) external view returns (address[] memory);
```

### Path To Base&#x20;

description

```solidity
function pathToBase(address asset) external view returns (address[] memory);
```

### Asset To Base

description

```solidity
function assetToBase(address asset, uint256 assetAmount) external view returns (uint256);
```

### Base To Asset

description

```solidity
function baseToAsset(address asset, uint256 baseAmount) external view returns (uint256);
```

### Asset To Asset&#x20;

description

```solidity
function assetToAsset(address fromAsset, address toAsset, uint256 fromAmount) external view returns (uint256);
```

### Asset To Tokens&#x20;

description

```solidity
function assetToTokens(address asset, uint256 floorPrice, uint256 assetAmount) external view returns (uint256);
```

### Tokens To Asset

description

```solidity
function tokensToAsset(address asset, uint256 floorPrice, uint256 tokenAmount) external view returns (uint256);
```

### Construct Path

description

```solidity
function constructPath(address from, address to) external view returns (address[] memory path);
```

### Get Floor Price

description

```solidity
function getFloorPrice(Assets memory assetDetails) external pure returns (uint64);
```

### Get Assets

description

```solidity
function getAssets(IKEI.Snapshot memory k) external view returns (Assets memory assetDetails);
```

### Get Prices

description

```solidity
function getPrices(Assets memory assets) external view returns (Prices memory priceDetails);
```

### Get Current Price Of

description

```solidity
function getCurrentPriceOf(IKEI.Snapshot memory k, address pair) external view returns (uint64);
```

### Get Reserve Evaluation

description

```solidity
function getReserveEvaluation(IKEI.Snapshot memory k) external view returns (uint128 totalBackingReserves, uint128 totalTokenReserves);
```

### Get Treasury Evaluation

description

```solidity
function getTreasuryEvaluation(IKEI.Snapshot memory k) external view returns (uint128 _evaluation, address _primaryAsset);
```

## Write Methods

### Update Paths

description

```solidity
function updatePaths(address _asset, address[] memory _pathFromBase, address[] memory _pathToBase) external;
```

### Update Ceiling Percent

description

```solidity
function updateCeilingPercent(uint256 _ceilingPercent) external;
```

### Update Evaluated Assets

description

```solidity
function updateEvaluatedAssets(address[] memory _evaluatedAssets) external;
```

## Events

### Ceiling Percent Updated

description

```solidity
event CeilingPercentUpdated(uint256 prevValue, uint256 newValue, address indexed sender);
```

### Evaluated Assets Updated

description

```solidity
event EvaluatedAssetsUpdated(address[] prevValue, address[] newValue, address indexed sender);
```

### Paths Updated

description

```solidity
event PathsUpdated(
    address[] prevFromPath,
    address[] newFromPath,
    address[] prevToPath,
    address[] newToPath,
    address indexed sender
);
```

## Structs

### Prices

description

```solidity
struct Prices {
    uint64 timestamp;
    uint64 floorPrice;
    uint64 currentPrice;
    uint64 ceilingPrice;
}
```

### Assets

description

```solidity
struct Assets {
    uint64 timestamp;
    address primaryAsset;
    // TOTALS
    uint128 tokensTotal;
    uint128 backingTotal;
    // CIRCULATING
    uint128 tokensCirculating;
    uint128 backingTreasury;
    // POOLS
    uint128 tokenReserves;
    uint128 backingReserves;
}
```
