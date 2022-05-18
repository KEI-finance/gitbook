---
description: description
---

# Access Control Upgradeable

## Read Methods

### Has Role

description

```solidity
function hasRole(bytes32 role, address account) external view returns (bool);
```

### Get Role Admin

description

```solidity
function getRoleAdmin(bytes32 role) external view returns (bytes32);
```

## Write Methods

### Grant Role

description

```solidity
 function grantRole(bytes32 role, address account) external;
```

### Revoke Role

description

```solidity
function revokeRole(bytes32 role, address account) external;
```

### Renounce Role&#x20;

description

```solidity
 function renounceRole(bytes32 role, address account) external;
```

## Events&#x20;

### Role Admins

description

```solidity
event RoleAdminChanged(bytes32 indexed role, bytes32 indexed previousAdminRole, bytes32 indexed newAdminRole);
```

### Role Granted&#x20;

description

```solidity
event RoleGranted(bytes32 indexed role, address indexed account, address indexed sender);
```

### Role Revoked

description

```solidity
event RoleRevoked(bytes32 indexed role, address indexed account, address indexed sender);
```
