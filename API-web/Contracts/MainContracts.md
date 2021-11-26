## Contracts
```javascript
   const contract = {
      *name, 
      description,
      symbol,
      *erc,
      decimals,
      maxSupply,
      adress,
      *campaignId,
      walletId
    };

    const project = await Mintknight.deployContract(contract);
```