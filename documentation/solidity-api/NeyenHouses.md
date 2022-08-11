# Solidity API

## NeyenHouses

This is the NFT contract of Neyen Houses

_This NFT contract is implemented with Chainlink VRF.
     The mint function isn't callable direcly by user but by one of Reseller contracts_

### _tokenIds

```solidity
struct Counters.Counter _tokenIds
```

### reseller

```solidity
address reseller
```

### maxSupply

```solidity
uint256 maxSupply
```

### linkFee

```solidity
uint256 linkFee
```

### keyHash

```solidity
bytes32 keyHash
```

### baseURI

```solidity
string baseURI
```

### lastTransferOf

```solidity
mapping(uint256 => uint256) lastTransferOf
```

### tokenIdToDNA

```solidity
mapping(uint256 => uint256) tokenIdToDNA
```

### VRFRequests

```solidity
mapping(bytes32 => uint256) VRFRequests
```

### HouseMinted

```solidity
event HouseMinted(uint256 tokenId, uint256 dna)
```

### constructor

```solidity
constructor(string _name, string _symbol, address _vrfCoordinator, address _link, bytes32 _keyHash, uint256 _linkFee, uint256 _maxSupply, address _feeReceiver) public
```

_The constructor of the NFT contract_

| Name | Type | Description |
| ---- | ---- | ----------- |
| _name | string | The name of the NFT collection |
| _symbol | string | The symbol of the NFT collection |
| _vrfCoordinator | address | The address of the Chainlink VRF contract |
| _link | address | The address of the LINK token contract |
| _keyHash | bytes32 | The hash required by the Chainlink VRF contract |
| _linkFee | uint256 | The cost fee of a VRF call |
| _maxSupply | uint256 | The NFT max supply |
| _feeReceiver | address | The NFT royalties receiver |

### mint

```solidity
function mint(address _receiver, uint256 _quantity) external
```

_This function processing mint of NFTs, it can be call only by the current reseller
     For each NFTs minted, a call to VRF coordinator is done_

| Name | Type | Description |
| ---- | ---- | ----------- |
| _receiver | address | The NFT receiver |
| _quantity | uint256 | The quantity of NFT to mint |

### fulfillRandomness

```solidity
function fulfillRandomness(bytes32 _requestId, uint256 _randomNumber) internal
```

_This function can be called only by Chainlink VRF contract
     It's the return of a random number request_

| Name | Type | Description |
| ---- | ---- | ----------- |
| _requestId | bytes32 | Chainlink VRF request identifier |
| _randomNumber | uint256 | The random number provided by Chainlink |

### dnaOf

```solidity
function dnaOf(uint256 _tokenId) public view returns (uint256)
```

_Function to get the token DNA_

| Name | Type | Description |
| ---- | ---- | ----------- |
| _tokenId | uint256 | The NFT token ID |

| Name | Type | Description |
| ---- | ---- | ----------- |
| [0] | uint256 | dna The DNA of the NFT |

### _baseURI

```solidity
function _baseURI() internal view returns (string)
```

_Internal function returning NFT base URI_

| Name | Type | Description |
| ---- | ---- | ----------- |
| [0] | string | dna NFT base URI |

### setBaseURI

```solidity
function setBaseURI(string __baseURI) public
```

_Function to set the NFT base URI, can be called only by the owner_

| Name | Type | Description |
| ---- | ---- | ----------- |
| __baseURI | string | The new NFT base URI |

### setReseller

```solidity
function setReseller(address _reseller) public
```

_Function to set the reseller address, can be called only by the owner_

| Name | Type | Description |
| ---- | ---- | ----------- |
| _reseller | address | The new reseller address |

### _beforeTokenTransfer

```solidity
function _beforeTokenTransfer(address from, address to, uint256 tokenId) internal
```

_Internal function executed before all transfers_

| Name | Type | Description |
| ---- | ---- | ----------- |
| from | address | address of the sender |
| to | address | address of the receiver |
| tokenId | uint256 | Token ID if the tranfered NFT |

### _burn

```solidity
function _burn(uint256 tokenId) internal
```

_Internal function executed before token burn_

| Name | Type | Description |
| ---- | ---- | ----------- |
| tokenId | uint256 | Token ID if the burned NFT |

### supportsInterface

```solidity
function supportsInterface(bytes4 interfaceId) public view returns (bool)
```

_Fixing multiple dependencies_

| Name | Type | Description |
| ---- | ---- | ----------- |
| interfaceId | bytes4 | interface id |

### tokenURI

```solidity
function tokenURI(uint256 tokenId) public view returns (string)
```

_Fixing multiple dependencies_

| Name | Type | Description |
| ---- | ---- | ----------- |
| tokenId | uint256 | Token ID |
