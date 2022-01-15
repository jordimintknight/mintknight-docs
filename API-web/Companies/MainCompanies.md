
Companies are entities linked to users. Each user can have up to one company. 

Only Authorized Users, can add / edit / fetch the information of their company:

Companies have the following fields:  

```javascript
 Companies: {
            name: 
            taxId: 
            address: 
            country: 
            createdAt:
            updatedAt: 
            model: { 'free', 'basic', 'company', 'agency'  },
            projectsAvailable: 
            projectsUsed: 
            contractsAvailable: 
            contractsUsed: 
            walletsAvailable: 
            walletsUsed:  
            mintsAvailable:  
            mintsUsed:  
            uploadsAvailable:  
            uploadUsed:  
            transfersAvailable:  
            transfersUsed: 
}
```


the required fields to create a company are the folloing fields:
name: 
taxId:

Free users, can create up to: 
3 projects
10 contracts
100 wallets
100 mints
10 uploads
1 transfer
