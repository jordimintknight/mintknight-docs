

{% swagger baseUrl="https://webapi.mintknight.com/" method="POST" path="contracts/:contractId/mint" summary="Mints a new NFT" %} {% swagger-description %} Mints a new NFT. {% endswagger-description %}

{% swagger-parameter in="body" name="name" required="true" type="string" %}  {% endswagger-parameter %}

{% swagger-parameter in="body" name="description" required="true" type="string" %} {% endswagger-parameter %}

{% swagger-parameter in="body" name="network" required="true" type="string" %} {% endswagger-parameter %}


{% swagger-response status="200" description="Project successfully created" %}

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
  // Mint 50 tokens to wallet 1.
  task = await mintknight.mintToken(
    project.contractId,
    minter.walletId,
    minter.skey,
	  wallet1.walletId,
	  '50',
  );
  task = await mintknight.waitTask(task.taskId);
```
{% endtab %}

{% tab title="Python" %}
```
# Install via pip
pip install --upgrade myapi
```
{% endtab %}
{% endtabs %}