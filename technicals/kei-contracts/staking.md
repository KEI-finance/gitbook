# Staking

### Files

* IStaking.sol
* Staking.sol

## Read Methods

### Max Stake Duration

Returns the maximum staking duration you can commit for, in seconds. (Applies to [Reward Multiplier](../../apps/staking/reward-multiplier.md))

```solidity
function MAX_STAKE_DURATION() external view returns (uint256);
```

### Min Stake Duration

Returns the minimum staking duration you can commit for, in seconds. (Applies to [Reward Multiplier](../../apps/staking/reward-multiplier.md))

```solidity
function MIN_STAKE_DURATION() external view returns (uint256);
```

### Max Reward Multiplier

Returns the maximum reward multiplier you can receive (in % form). (Applies to [Reward Multiplier](../../apps/staking/reward-multiplier.md))

```solidity
function MAX_REWARD_MULTIPLIER() external view returns (uint256);
```

### Min Reward Multiplier

Returns the minimum reward multiplier you can receive (in % form). (Applies to [Reward Multiplier](../../apps/staking/reward-multiplier.md))

```solidity
function MIN_STAKE_DURATION() external view returns (uint256);
```

### Gradient

Returns the steepness of the [Reward Curve](../../apps/staking/reward-multiplier.md#reward-curve), and [Penalty Curve](../../apps/staking/unstake-penalty.md#penalty-curve).

```solidity
function MIN_STAKE_DURATION() external view returns (uint256);
```

### Total Rewards

Returns how many rewards (tokens) the staking contract is currently holding onto.

```solidity
function totalRewards() external view returns (uint256);
```

### Details Of

Returns the [StakeDetails](staking.md#undefined) of a stake, given the _stakeId_.

```solidity
function detailsOf(uint256 stakeId) external view returns (StakeDetails memory);
```

### Gradient

The steepness of the [Reward Curve](../../apps/staking/reward-multiplier.md#reward-curve), and [Penalty Curve](../../apps/staking/unstake-penalty.md#penalty-curve).

```solidity
function MIN_STAKE_DURATION() external view returns (uint256);
```

### Gradient

The steepness of the [Reward Curve](../../apps/staking/reward-multiplier.md#reward-curve), and [Penalty Curve](../../apps/staking/unstake-penalty.md#penalty-curve).

```solidity
function MIN_STAKE_DURATION() external view returns (uint256);
```

## Write Methods

## Events

## Structs

### Stake Details

Contains all of the information about a particular stake.

```solidity
struct StakeDetails {
    address creator;
    uint32 rewardMultiplier;
    
    uint128 currentSupply;
    uint128 initialSupply;
    
    uint64 createdAt;
    uint64 expiresAt;
    uint64 stakeDuration;
    uint64 lockDuration;
}
```

