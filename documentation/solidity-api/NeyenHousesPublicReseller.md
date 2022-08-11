# Solidity API

## NeyenHousesPublicReseller

This is the public reseller contract

_This contract implement the public minting logic and inherite from NeyenHousesReseller for implement selling_

### constructor

```solidity
constructor(address _neyenHouses, address _resellerStorage) public
```

_The constructor of the reseller contract. The contract is paused when it is deployed_

| Name | Type | Description |
| ---- | ---- | ----------- |
| _neyenHouses | address | address of the NFT collection |
| _resellerStorage | address | address of the reseller storage |

### mint

```solidity
function mint(uint256 _amount) external
```

_The public mint function._

| Name | Type | Description |
| ---- | ---- | ----------- |
| _amount | uint256 | Amount of NFTs to mint |
