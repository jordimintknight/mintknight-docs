
### Transfer one NFT

{% swagger baseUrl="https://api.mintknight.com/" method="PUT" path="nfts" summary="Transfer a NFT" %} {% swagger-description %} Transfer a NFT {% endswagger-description %}

{% swagger-parameter in="body" name="name" required="true" type="string" %} The .... {% endswagger-parameter %}


{
   
}
{% endswagger-response %}

{% swagger-response status="401" description="Permission denied" %}

{% endswagger-response %} {% endswagger %}



{% tabs %}
{% tab title="Node" %}
```javascript

  // Transfer an NFT
  let nft = await mintknight.mintNFT(
      ContractId,
      walletId,
      skey,
      to,
      metadata      
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
