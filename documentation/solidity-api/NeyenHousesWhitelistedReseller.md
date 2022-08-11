# Solidity API

## NeyenHousesWhitelistedReseller

This is the whitelisted reseller contract

_This contract implement the whitelisting with merkle proof logic and inherite from NeyenHousesReseller for implement selling_

### merkleRoot

```solidity
bytes32 merkleRoot
```

### OnlyWhitelisted

```solidity
modifier OnlyWhitelisted(uint256 index, bytes32[] merkleProof)
```

### constructor

```solidity
constructor(address _neyenHouses, address _resellerStorage) public
```

_The constructor of the whitelisted reseller contract._

| Name | Type | Description |
| ---- | ---- | ----------- |
| _neyenHouses | address | address of the NFT collection |
| _resellerStorage | address | address of the reseller storage |

### setMerkleRoot

```solidity
function setMerkleRoot(bytes32 _merkleRoot) external
```

_The constructor of the whitelisted reseller contract._

| Name | Type | Description |
| ---- | ---- | ----------- |
| _merkleRoot | bytes32 | the new merkle root to use for whitelisting |

### mint

```solidity
function mint(uint256 _amount, uint256 _index, bytes32[] _merkleProof) external
```

_The whitelisted mint function._

| Name | Type | Description |
| ---- | ---- | ----------- |
| _amount | uint256 | Amount of NFTs to mint |
| _index | uint256 | User index in the merkle tree |
| _merkleProof | bytes32[] | index proof in the merkle tree |


### neyenHouses

```solidity
function neyenHouses() external view returns (address)
```

### housesMintedBy

```solidity
function housesMintedBy(address user_) external view returns (uint256)
```

### increaseHousesMintedBy

```solidity
function increaseHousesMintedBy(address user_, uint256 housesMinted) external
```
