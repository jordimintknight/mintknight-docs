### Get Wallet info (NFTS + tokens)


@return a Wallet object

{% swagger baseUrl="https://serviceapi.mintknight.com/" method="get" path="wallets/:walletId" summary="Get one wallet and its content - nfts and tokens" %} {% swagger-description %} Get one wallet and its content - nfts and tokens. {% endswagger-description %}

{% swagger-parameter in="header" name="Content-Type" required="true" type="string" %} A string indicating the media type of the resource {% endswagger-parameter %}

{% swagger-parameter in="header" name="x-api-key" required="true" type="string" %} Authentication token {% endswagger-parameter %}

{% swagger-parameter in="body" name="walletId" required="true" type="string" %} The id of the wallet {% endswagger-parameter %}

{% swagger-parameter in="body" name="network" required="true" type="string" %} the network {% endswagger-parameter %}

{% swagger-parameter in="body" name="adress" required="true" type="string" %} The adressof the wallet {% endswagger-parameter %}




{% swagger-response status="200" description="Wallet successfully added" %}

{

}
{% endswagger-response %}

{% swagger-response status="401" description="Permission denied" %}

{% endswagger-response %} {% endswagger %}




{% tabs %}
{% tab title="Node" %}
```javascript

  // Check Balance for Both wallets
  let wallet1 = await mintknight.getWallet(wallet1Id);
  console.log(wallet1);
  wallet2 = await mintknight.getWallet(wallet2Id);
  console.log(wallet2);
  
```
{% endtab %}

{% tab title="Python" %}
```
# Install via pip
pip install --upgrade myapi
```
{% endtab %}
{% endtabs %}

