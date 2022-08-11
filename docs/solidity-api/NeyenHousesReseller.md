# Solidity API

## NeyenHousesReseller

This is the main reseller contract

_This contract implement the reseller logic and will be inherited by public and whitelisted reseller contracts_

### neyenHouses

```solidity
contract INeyenHouses neyenHouses
```

### resellerStorage

```solidity
contract INeyenHousesResellerStorage resellerStorage
```

### payableWith

```solidity
contract IERC20 payableWith
```

### maxResellerSupply

```solidity
uint256 maxResellerSupply
```

### housePrice

```solidity
uint256 housePrice
```

### perAddressLimit

```solidity
uint256 perAddressLimit
```

### constructor

```solidity
constructor(address _neyenHouses, address _resellerStorage) public
```

_The constructor of the reseller contract. The contract is paused when it is deployed_

| Name | Type | Description |
| ---- | ---- | ----------- |
| _neyenHouses | address | address of the NFT collection |
| _resellerStorage | address | address of the reseller storage |

### pause

```solidity
function pause() public
```

_Pause the contract (can't sell anymore)_

### unpause

```solidity
function unpause() public
```

_Unpause the contract (open selling)_

### setConfig

```solidity
function setConfig(uint256 _maxResellerSupply, uint256 _perAddressLimit, uint256 _housePrice, address _payableWith) external
```

_Set the config of the reseller. The contract is paused when this function is called_

| Name | Type | Description |
| ---- | ---- | ----------- |
| _maxResellerSupply | uint256 | total supply limit for this reseller based on the NFT collection total supply |
| _perAddressLimit | uint256 | limit of NFT minted by an address based on the reseller storage data |
| _housePrice | uint256 | The unit cost of an NFT mint |
| _payableWith | address | the ERC20 token address used for pay the NFT mint |

### getBuyableOf

```solidity
function getBuyableOf(address _address) external view returns (uint256)
```

_Get the remaining NFT mintable by an address_

| Name | Type | Description |
| ---- | ---- | ----------- |
| _address | address | address of the user |

### _mint

```solidity
function _mint(uint256 _amount) internal
```

_Internal function for minting an NFT_

| Name | Type | Description |
| ---- | ---- | ----------- |
| _amount | uint256 | amount of NFTs to mint |

### withdrawERC20

```solidity
function withdrawERC20(address _token) public
```

_Withdraw ERC2O owned  by the contract to the sender._

| Name | Type | Description |
| ---- | ---- | ----------- |
| _token | address | address of the ERC20 to withdraw |
