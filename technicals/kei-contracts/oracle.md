---
description: description
---

# Oracle

## Read Methods

### Manage Role

description

```solidity
function MANAGE_ROLE() external view returns (bytes32);
```

### Snapshot

description

```solidity
 function snapshot(uint256 index) external view returns (Snapshot memory);
```

### Total Snapshots

description

```solidity
function totalSnapshots() external view returns (uint256);
```

### Latest Snapshot

description

```solidity
function latestSnapshot() external view returns (Snapshot memory);
```

### Snapshot At&#x20;

description

```solidity
 function snapshotAt(uint256 timestamp) external view returns (Snapshot memory);
```

### Prices

description

```solidity
function prices() external view returns (IPricing.Prices memory);
```

### Prices Of&#x20;

description

```solidity
function pricesOf(IKEI.Snapshot memory k, address pair) external view returns (IPricing.Prices memory);
```

### Prices At

description

```solidity
function pricesAt(uint256 timestamp) external view returns (IPricing.Prices memory);
```

### Cumulative Price Last

description

```solidity
 function cumulativePriceLAST() external view returns (uint256);
```

### Assets

description

```solidity
 function assets() external view returns (IPricing.Assets memory);
```

### Primary Asset&#x20;

description

```solidity
function primaryAsset() external view returns (address);
```

### Scan&#x20;

description

```solidity
function scan(uint256 startFrom, uint256 total) external view returns (Snapshot[] memory results);
```

### Avg Price From

description

```solidity
function avgPriceFrom(uint256 timestamp) external view returns (uint256);
```

## Write Methods

### Create Snapshot

description

```solidity
 function createSnapshot(IKEI.Snapshot memory k) external returns (IPricing.Prices memory prices);
```

## Events

### Snapshot Created

description

```solidity
event SnapshotCreated(uint256 timestamp);
```

## Structs

### Snapshot

description

```solidity
struct Snapshot {
    uint64 timestamp;
    IPricing.Prices prices;
    IPricing.Assets assets;
    uint256 cumulativePriceLAST;
}
```
