# Solidity API

## NeyenHousesResellerStorage

This is the resellers storage contract

_This contract store the number of NFT bought by addresses_

### neyenHouses

```solidity
contract INeyenHouses neyenHouses
```

### housesMintedByAddress

```solidity
mapping(address => uint256) housesMintedByAddress
```

### onlyReseller

```solidity
modifier onlyReseller()
```

### constructor

```solidity
constructor(address _neyenHouses) public
```

_The constructor of the reseller storage contract_

| Name | Type | Description |
| ---- | ---- | ----------- |
| _neyenHouses | address | address of the NFT collection |

### housesMintedBy

```solidity
function housesMintedBy(address _user) external view returns (uint256)
```

_Function returning the number of NFT minted by an address_

| Name | Type | Description |
| ---- | ---- | ----------- |
| _user | address | address of the user |

| Name | Type | Description |
| ---- | ---- | ----------- |
| [0] | uint256 | uint256 the number of NFT already minted |

### increaseHousesMintedBy

```solidity
function increaseHousesMintedBy(address _user, uint256 _housesMinted) external
```

_Function for increase the number of NFT minted by an address. Only callable by the current reseller_

| Name | Type | Description |
| ---- | ---- | ----------- |
| _user | address | address of the user |
| _housesMinted | uint256 | increase number |
