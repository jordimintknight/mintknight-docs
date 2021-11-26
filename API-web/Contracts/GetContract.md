{% swagger baseUrl="https://webapi.mintknight.com/" method="GET" path="contracts/:contractId" summary="fetch a contract" %} {% swagger-description %} fetch a contract. {% endswagger-description %}


{% swagger-response status="200" description="Contract successfully created" %}

{
    "_id": "XXXXXXXXXXXX...XX",
    "name": "the name of a project",
    "description": "this is the project description",
    "network": "the network your project is working",
    "createdAt": "2021-11-05T05:24:15.026Z",
    "updatedAt": "2021-11-05T05:24:15.026Z",
    "companyId": "Company_ID",
    "createdBy": "User_ID",
    "__v": 0
}
{% endswagger-response %}

{% swagger-response status="401" description="Permission denied" %}

{% endswagger-response %} {% endswagger %}


{% tabs %}
{% tab title="Node" %}
```javascript

  // GET a contract
  let contract = await mintknight.getContract(
      ContractId
      );
   
```
{% endtab %}

{% tab title="Python" %}
```
# Install via pip
pip install --upgrade myapi
```
{% endtab %}
{% endtabs %}
