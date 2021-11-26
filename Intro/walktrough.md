---
description: 
---
In this page we will start introducing you to the resources our API provides. This brief description will help conceptualize what is each resource, and what role plays in the mintknight platform.  

## Users and Companies
These are the users in your company, responsible to create Projects, collections and NFTs drops.
A user must have an associated company. Projects belong to the user and the company.

Roles for users in companies:

- admin (invoice info, projects)
- manager (campaigns/collections)
- Minter (can mint NFTs)

WIP: You can also create an API KEY specific for minting collections

## Projects
The top level in every NFT campaigns.

## Collection
Projects are organizaed in collections (sublevel 1). Every Collection can have many NFTs drops.

A collection is an ERC721 or an ERC1155 Contract.

Whenever a Drop is created it starts in draft mode. While in draft, it can be edited, as the NFT Contract is not yet in the Blockchain (deployed). But once it is deployed it cannot be changed anymore.

## Tokens


## NFTs and Wallets
Before minting an NFT you need to create a Wallet for the user reciving the NFT. Every wallet will be encrypted with a password known only to the company.

WIP: Every time a transaction is made, the password will can be changed.

WIP: Recovery Strategy, we are using Shamir Secret Sharing to create three encrypted parts of the Private Key with 2/3 to recover. At Mintknight we keep one, the company will keep the second and the third will be sent to the end user to keep (email, for example). It's up to the company to send the 3rd part to the user.

Once the wallet is created it's time to mint the NFT and send it to the Blockchain.

The static metadata for every NFT is : title, description and image.
** Remember that once minted this data cannot be Changed **

Every NFT has also associated a dynamic metadata (a link inside the static metadata), that can be changed at anytime by the users in the company with access to that collection.

To transfer an NFT, the password to that wallet must be provided in order to send the transaction to the Blockchain.

## Additional Information

[Ethereum NFTs](/blockchain/ethereum)
