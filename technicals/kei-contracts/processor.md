---
description: description
---

# Processor

## Read Methods

### Process

description

```solidity
function process(address recipient, uint256 rewardsToProcess) external;
```

## Events

### Work Completed

description

```solidity
event WorkCompleted(address indexed recipient, uint256 totalRewards, Task[] jobs);
```

## Structs

### Task

description

```solidity
struct Task {
    bytes32 id;
    bool success;
    bytes error;
}
```
