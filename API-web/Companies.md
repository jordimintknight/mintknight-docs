

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

### Post Companies

{% swagger baseUrl="https://webapi.mintknight.com/" method="post" path="companies/" summary="Add a new Company." %} {% swagger-description %} Add a new Company. {% endswagger-description %}

{% swagger-parameter in="body" name="token" required="true" type="string" %} The bearer token that authentificates a user {% endswagger-parameter %}

{% swagger-parameter in="body" name="name" required="true" type="string" %} The name of the company {% endswagger-parameter %}

{% swagger-parameter in="body" name="taxId" required="true" type="string" %} The Tax Id of the company {% endswagger-parameter %}

{% swagger-parameter in="body" name="adress" required="true" type="string" %} The adress of the company {% endswagger-parameter %}

{% swagger-parameter in="body" name="country" required="true" type="string" %} The Country of the company {% endswagger-parameter %}


{% swagger-response status="200" description="Campaign successfully created" %}

{
    "model": "free",
    "projectsAvailable": 1,
    "projectsUsed": 0,
    "contractsAvailable": 10,
    "contractsUsed": 0,
    "walletsAvailable": 100,
    "walletsUsed": 0,
    "mintsAvailable": 100,
    "mintsUsed": 0,
    "uploadsAvailable": 10,
    "uploadUsed": 0,
    "transfersAvailable": 1,
    "transfersUsed": 0,
    "_id": "XXXX....XXXX",
    "name": "Test Company",
    "taxId": "XXXXXXX",
    "country": "Company country",
    "createdAt": "2021-11-05T04:39:26.861Z",
    "updatedAt": "2021-11-05T04:39:26.861Z",
    "__v": 0
}
{% endswagger-response %}

{% swagger-response status="401" description="Permission denied" %}

{% endswagger-response %} {% endswagger %}



### Get Companies

To fetch all the information of a user comapny: 

{% swagger baseUrl="https://webapi.mintknight.com/" method="GET" path="companies/" summary="Get the Company information." %} {% swagger-description %} Get the Company information. {% endswagger-description %}

{% swagger-parameter in="body" name="token" required="true" type="string" %} you have to pass a bearer token in the header for authentification {% endswagger-parameter %}

{% swagger-response status="200" description="Companie successfully fetched" %}

{
    "model": "free",
    "projectsAvailable": 1,
    "projectsUsed": 0,
    "contractsAvailable": 10,
    "contractsUsed": 0,
    "walletsAvailable": 100,
    "walletsUsed": 0,
    "mintsAvailable": 100,
    "mintsUsed": 0,
    "uploadsAvailable": 10,
    "uploadUsed": 0,
    "transfersAvailable": 1,
    "transfersUsed": 0,
    "_id": "6184b57e7771000019c8de34",
    "name": "Test Company",
    "taxId": "2222222",
    "country": "nicaragua",
    "createdAt": "2021-11-05T04:39:26.861Z",
    "updatedAt": "2021-11-05T04:39:26.861Z",
    "__v": 0
}
{% endswagger-response %}

{% swagger-response status="401" description="Permission denied" %}

{% endswagger-response %} {% endswagger %}


```javascript
const MintknightWeb = require('mintknight-web');

const companyInfo =  async MintknightWeb.getCompany(user) 
```
