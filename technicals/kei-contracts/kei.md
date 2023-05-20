---
description: The main application container, holding all of the contract locations
---

# Kei

{% hint style="info" %}
The main source of truth. Will be used throughout the protocol as the source of truth to identify all of the main contracts.
{% endhint %}

### Files

* [IKEI.sol](https://github.com/kevupton/kei-finance/blob/master/solidity/contracts/kei/IKEI.sol)
* [KEI.sol](https://github.com/kevupton/kei-finance/blob/master/solidity/contracts/kei/KEI.sol)

## Read Methods

### Master

The master address, responsible for upgrading the protocol, and ensuring security.

```solidity
function master() external view returns (address);
```

### Token

Returns the [Token](token.md) contract for the Kei Protocol.

```solidity
function token() external view returns (IKEIToken);
```

### Pair Controller

Returns the [PairController](pair-controller.md)

```solidity
function pairController() external view returns (IPairController);
```

### Liquidity Controller

Returns the [LiquidityController](liquidity-controller.md)

```solidity
function liquidityController() external view returns (ILiquidityController);
```

### Token Controller

Returns the [TokenController](token-controller.md)

```solidity
function tokenController() external view returns (ITokenController);
```

### Staking

Returns the [Staking](staking.md). Or [read how it works.](../../applications/staking/)

```solidity
function staking() external view returns (IStaking);
```

### Treasury

Returns the [Treasury](treasury.md)

```solidity
function treasury() external view returns (ITreasury);
```

### Bonding

Returns the [Bonding](bonding.md). Or [read how it works.](../../applications/bonding.md)

```solidity
function bonding() external view returns (IBonding);
```

### Oracle

Returns the [Oracle](oracle.md)

```solidity
function oracle() external view returns (IOracle);
```

### Fees

Returns the [Fees](fees.md)

```solidity
function fees() external view returns (IFees);
```

### Admin

Returns the [Admin](admin.md)

```solidity
function admin() external view returns (IAdmin);
```

### Affiliate

Returns the [Affiliate](affiliate.md)

```solidity
function affiliate() external view returns (IAffiliate);
```

### Processor

Returns the [Processor](processor.md)

```solidity
function processor() external view returns (IProcessor);
```

### Pricing

Returns the [Pricing](pricing.md)

```solidity
function pricing() external view returns (IPricing);
```

### Rewards

Returns the [Rewards](rewards.md)

```solidity
function rewards() external view returns (IRewards);
```

### Debt

Returns the [Debt](debt.md)

```solidity
function debt() external view returns (IDebt);
```

### Snapshot Hash

Returns the snapshot hash, which represents, the hash of the entire snapshot state of the Kei contract.&#x20;

```solidity
function snapshotHash() external view returns (bytes32);
```

Calculated by taking a **keccak256** of the `IKEI.Snapshot`

```solidity
snapshotHash = keccak256(abi.encode(_snapshot));
```

### Paused

Returns the status of the protocol. Whether or not it is paused.

```solidity
function paused() external view returns (bool);
```

## Write Methods

### Pause&#x20;

An additional security functionality, for pausing the protocol in case of an emergency, preventing any major actions from taking place. Only used to prevent further damage from being done to the protocol.&#x20;

{% hint style="info" %}
Only callable via the Master address.
{% endhint %}

```solidity
function pause() external onlyMaster;
```

### Unpause

Resumes functionality as before

{% hint style="info" %}
Only callable via the Master address.
{% endhint %}

```solidity
function unpause() external onlyMaster;
```

