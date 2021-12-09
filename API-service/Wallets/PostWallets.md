### Add Wallet 
@return a Wallet object

{% swagger baseUrl="https://serviceapi.mintknight.com/" method="post" path="wallets" summary="Deploy a new wallet" %} {% swagger-description %} Deploys a new wallet. {% endswagger-description %}

{% swagger-parameter in="header" name="Content-Type" required="true" type="string" %} A string indicating the media type of the resource {% endswagger-parameter %}

{% swagger-parameter in="header" name="x-api-key" required="true" type="string" %} Authentication token {% endswagger-parameter %}

{% swagger-parameter in="body" name="companyId" required="true" type="string" %} The id of the company adding a wallet {% endswagger-parameter %}

{% swagger-parameter in="body" name="owner" required="true" type="string" %} The id of the user adding a wallet {% endswagger-parameter %}

{% swagger-parameter in="body" name="network" required="true" type="string" %} The id of the user adding a wallet {% endswagger-parameter %}

{% swagger-parameter in="body" name="skey" required="true" type="string" %} The id of the user adding a wallet {% endswagger-parameter %}

{% swagger-parameter in="body" name="refUser" required="true" type="string" %} The id of the user adding a wallet {% endswagger-parameter %}

{% swagger-response status="200" description="Wallet successfully added" %}

{

}
{% endswagger-response %}

{% swagger-response status="401" description="Permission denied" %}

{% endswagger-response %} {% endswagger %}




{% tabs %}
{% tab title="Node" %}
```javascript

  let task = await mintknight.addWallet('id_minter');
  const minter = { walletId: task.wallet._id, skey: task.skey1 };
  task = await mintknight.waitTask(task.taskId);
  minter.address = task.addressTo;


```
{% endtab %}

{% tab title="Python" %}
```
# Install via pip
pip install --upgrade myapi
```
{% endtab %}
{% endtabs %}


