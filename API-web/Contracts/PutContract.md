
{% swagger baseUrl="https://webapi.mintknight.com/" method="PUT" path="contracts/:contractId" summary="Updates a contract" %} {% swagger-description %} Updates a Contract. {% endswagger-description %}
{% swagger-parameter in="body" name="name" required="true" type="string" %} The name of the contract {% endswagger-parameter %}

{% swagger-parameter in="body" name="symbol" required="false" type="string" %} The Symbol of the Contract {% endswagger-parameter %}

{% swagger-parameter in="body" name="description" required="true" type="string" %} The description of the Contract {% endswagger-parameter %}

{% swagger-parameter in="body" name="decimal" required="false" type="string" %} decimals of Contract {% endswagger-parameter %}

{% swagger-parameter in="body" name="network" required="true" type="string" %} The network of the Contract {% endswagger-parameter %}

{% swagger-parameter in="body" name="adress" required="false" type="string" %} the adress of the contract {% endswagger-parameter %}

{% swagger-parameter in="body" name="erc" required="false" type="string" %} erc {% endswagger-parameter %}

{% swagger-parameter in="body" name="maxSupply" required="false" type="string" %} Max supply {% endswagger-parameter %}

{% swagger-parameter in="body" name="totalSupply" required="false" type="string" %} Total Supply {% endswagger-parameter %}

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