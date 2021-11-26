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


{% tabs %}
{% tab title="Node" %}
```javascript
const MintknightWeb = require('mintknight-web');

const companyInfo =  async MintknightWeb.getCompany(user) 
```
{% endtab %}

{% tab title="Python" %}
```
# Install via pip
pip install --upgrade myapi
```
{% endtab %}
{% endtabs %}

