

Companies are entities linked to users. Each user can have up to one company. 
The company object have the follwing structure:  

```javascript
  const company = await mintknight.setCompany(
    COMPANY_NAME,
    COMPANY_TAXID,
    COMPANY_ADDRESS,
    COMPANY_COUNTRY,
  );
```


Only logged in Users, can add / edit / fetch the information of their company:





```javascript
const MintknightWeb = require('mintknight-web');

const companyInfo =  async MintknightWeb.getCompany(user) 
```
