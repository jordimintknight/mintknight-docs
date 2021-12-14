## Contracts

In this level, you decide what type of contract are you gonna use for the drops belonging to this contract
('MKERC29', 'MKERC721', 'MKVoucher') are some of our contracts

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
      *walletId
    };

    const project = await Mintknight.deployContract(contract);
```
