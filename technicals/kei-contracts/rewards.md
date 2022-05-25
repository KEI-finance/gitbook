---
description: description
---

# Rewards

## Read Methods

### Manage Role

description

```solidity
function MANAGE_ROLE() external view returns (bytes32);
```

### Admin Role

description

```solidity
function ADMIN_ROLE() external view returns (bytes32);
```

### Percentages

description

```solidity
function percentages() external view returns (RewardPercentages memory);
```

## Write Methods

### Update Percentages

description

```solidity
function updatePercentages(RewardPercentages memory percentages_) external;
```

### Sync

description

```solidity
 function sync(IKEI.Snapshot memory k) external;
```

### Process

description

```solidity
function process(IKEI.Snapshot memory k, uint256 totalToProcess) external;
```

## Events

### Reward Percentages Updated

description

```solidity
  event RewardPercentagesUpdated(RewardPercentages prevValues, RewardPercentages newValues, address indexed sender);
```

### Reward Created

description

```solidity
 event RewardCreated(Reward reward);
```

### Rewards Distributed

description

```solidity
event RewardsDistributed(RewardDistributions distributions, uint256 totalProcessed, address indexed sender);
```

## Structs

### Reward

description

```solidity
struct Reward {
    RewardPercentages percentages;
    uint256 totalReward;
    address txOrigin;
    uint64 timestamp;
}
```

### Reward Percentages

description

```solidity
struct RewardPercentages {
    uint16 debtPercent;
    uint16 adminPercent;
    uint16 workerPercent;
    uint16 stakingPercent;
    uint16 affiliatePercent;
    uint16 liquidityPercent;
    uint16 treasuryPercent;
}
```

### Reward Distributions

description

```solidity
struct RewardDistributions {
    uint256 adminTokens;
    uint256 affiliateTokens;
    uint256 stakingTokens;
    uint256 liquidityTokens;
    uint256 workerTokens;
    uint256 debtTokens;
    uint256 treasuryTokens;
}
```
