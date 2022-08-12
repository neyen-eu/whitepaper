# Contracts

## Vente des NFTs

Pour cette etape, il y aura 4 smart contracts de déployé:
  - NeyenHouses: Le contrat ERC721 de la collection
  - NeyenHousesWhitelistedReseller: Le contrat qui servira de point de vente de la vente privé avec whitelist implementé avec un merkleroot
  - NeyenHousesPublicReseller: Le contrat qui servira de point de vente de la vente public
  - NeyenHousesResellerStorage: Le contrat servant de stockage distribué entre les contrats NeyenHousesWhitelistedReseller et NeyenHousesPublicReseller

## Adresse des smart contrats

### Rinkeby

| Contrats                      | Adresse                                     |
|--------------------------------|---------------------------------------------|
| NeyenHouses                    | [0x942ae16dfaddae2a04887edd50d3d33781b37ee3](https://rinkeby.etherscan.io/address/0x942ae16dfaddae2a04887edd50d3d33781b37ee3), |
| NeyenHousesWhitelistedReseller | [0x31395F35533A10EAfb27f8a631b2F1D26c8FCBbd](https://rinkeby.etherscan.io/address/0x31395F35533A10EAfb27f8a631b2F1D26c8FCBbd)  |
| NeyenHousesPublicReseller      | [0xDeb6073598483676fbce58846e3739B0E42c4Fe5](https://rinkeby.etherscan.io/address/0xDeb6073598483676fbce58846e3739B0E42c4Fe5)  |
| NeyenHousesResellerStorage     | [0x5c086371495d437e607f6dcb6625a28d736e95d0](https://rinkeby.etherscan.io/address/0x5c086371495d437e607f6dcb6625a28d736e95d0)  |
