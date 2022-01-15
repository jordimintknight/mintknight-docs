### Post Companies

{% swagger baseUrl="https://webapi.mintknight.com/" method="post" path="companies/" summary="Add a new Company." %} {% swagger-description %} Add a new Company. {% endswagger-description %}

{% swagger-parameter in="header" name="Content-Type" required="true" type="string" %} A string indicating the media type of the resource {% endswagger-parameter %}

{% swagger-parameter in="header" name="x-api-key" required="true" type="string" %} Authentication token {% endswagger-parameter %}

{% swagger-parameter in="body" name="name" required="true" type="string" %} The name of the company {% endswagger-parameter %}

{% swagger-parameter in="body" name="taxId" required="true" type="string" %} The Tax Id of the company {% endswagger-parameter %}

{% swagger-parameter in="body" name="adress" type="string" %} The adress of the company {% endswagger-parameter %}

{% swagger-parameter in="body" name="country" type="string" %} The Country of the company {% endswagger-parameter %}


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


{% tabs %}
{% tab title="Node" %}
```javascript
  const company = await mintknight.setCompany(
    COMPANY_NAME,
    COMPANY_TAXID,
    COMPANY_ADDRESS,
    COMPANY_COUNTRY,
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
