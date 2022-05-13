# Staking

### Files

* IStaking.sol
* Staking.sol

## Read Methods

### Manage Role

Returns the hash of the manage role. Used in updating the [NFTDescriptor](staking.md#nft-descriptor) for the Staking contract.

```solidity
function MANAGE_ROLE() external view returns (bytes32);
```

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

### Decimals

Returns how many decimals to associate with your Stake balance

```solidity
function decimals() external pure returns (uint8);
```

### Total Supply

Returns the total supply of all stake tokens created

```solidity
function totalSupply() external view returns (uint256);
```

### Total Rewards

Returns how many rewards (tokens) the staking contract is currently holding onto.

```solidity
function totalRewards() external view returns (uint256);
```

### Total Value

Returns the total value of the entire stake pool. Including the modifier of the multiplier.

```solidity
function totalValue() external view returns (uint256);
```

### Total Multiplied

Returns the sum of all the stakes multiplied by their associated multiplier. Used in the calculations of the Staking contract. [Read More](../../apps/staking/staking-calculations.md)

```solidity
function totalMultiplied() external view returns (uint256);
```

### Total Stakes Created

Returns the total number of stakes that have been created to date. Includes stakes that have already been unstaked.

```solidity
function totalStakesCreated() external view returns (uint256);
```

### Balance Of (Users Total Balance)

Returns the total stake balance of an account.

```solidity
function balanceOf(address account) external view returns (uint256);
```

### Balance Of (Users Stake Balance)

Returns the amount that an account owns of a particular stake

```solidity
function MIN_STAKE_DURATION() external view returns (uint256);
```

### Unstake Penalty Of

Returns the % penalty from unstaking a particular stake. Refer to [Unstake Penalty](../../apps/staking/unstake-penalty.md) for the math. The % Value is in the format of `type(uint16).max`

```solidity
function MIN_STAKE_DURATION() external view returns (uint256);
```

### Reward Balance Of (Account)

Returns the total token value of a stake, based on an accounts balance of it

```solidity
function rewardBalanceOf(address account, uint256 stakeId) external view returns (uint256);
```

### Reward Balance Of (Any)

Returns the total token value of a stake, based on the amount of stake input

```solidity
function rewardBalanceOf(uint256 stakeId, uint256 amount) external view returns (uint256);
```

### Estimated Unstake Rewards

Returns the _principle_ (initial investment), _rewards_ (rewards from staking), _unstake penalty_ (penalty which is subtracted from the _principle_ and _rewards_)

```solidity
function estimateUnstakeRewards(uint256 stakeId, uint256 amount) 
external 
view
returns (
     uint256 principle, 
     uint256 rewards,
     uint256 unstakePenalty
 );
```

### Get Stake

Returns the [StakeDetails](staking.md#undefined) of a stake, given the _stakeId_.

```solidity
function detailsOf(uint256 stakeId) external view returns (StakeDetails memory);
```

### NFT Descriptor

Returns the location of the [NFTDescriptor](nft-descriptor.md) contract. Used in generating the metadata for the [NFT Stake](../../apps/staking/staking-nfts.md).

```solidity
function nftDescriptor() external view returns (address);
```

## Write Methods

### Stake

Creates a stake position, based on the following input. Requires that tokens are sent to the [Treasury](treasury.md), prior to being called. (It will Stake how ever many tokens the treasury receives).

* _account_ - the account receiving the stake
* _stakeDuration_ - used in calculating the [Reward Multiplier](../../apps/staking/reward-multiplier.md) for the stake.
* _lockDuration_ - used to force a minimum stake duration with no benefits to the [Reward Multiplier.](../../apps/staking/reward-multiplier.md)

```solidity
function stake(
    address account, 
    uint256 stakeDuration, 
    uint256 lockDuration
) external returns (uint256);
```

### Unstake

Unstakes a certain amount of a particular stake. Returning the [Estimated Unstake Rewards](staking.md#estimated-unstake-rewards) back to the sender.

```solidity
function unstake(uint256 stakeId, uint256 amount) external returns (uint256);
```

### Set NFT Descriptor

Only callable by an account that has the [Manage Role](staking.md#max-stake-duration). It will update the [NFT Descriptor](nft-descriptor.md) for the Staking contract, which is responsible for generating the NFT Metadata.

```solidity
function setNFTDescriptor(address newDescriptor) external;
```

## Events

### NFT Descriptor Updated

Emitted when the [NFTDescriptor](staking.md#undefined) for the Staking contract has been updated.

```solidity
event NFTDescriptorUpdated(
    address indexed prevValue, 
    address indexed newValue, 
    address indexed sender
);
```

### Stake Created

Emitted when a new Stake has been created.

```solidity
event StakeCreated(
    uint256 indexed stakeId,
    address indexed forAccount,
    uint256 lockDuration,
    uint256 stakeDuration,
    address sender
);
```

### Stake Removed

Emitted when a Stake has been unstaked

```solidity
event StakeRemoved(
    uint256 indexed stakeId,
    uint256 amount,
    uint256 principle,
    uint256 rewards,
    uint256 unstakePenalty,
    address indexed sender
);
```

## Structs

### Stake Details

Contains all of the information about a particular stake.

```solidity
struct Stake {
    uint32 rewardMultiplier;
    uint112 principle;
    uint112 totalSupply;
    
    uint256 rewardsStart;
    
    uint64 createdAt;
    uint64 expiresAt;
    uint64 stakeDuration;
    uint64 lockDuration;
}
```



