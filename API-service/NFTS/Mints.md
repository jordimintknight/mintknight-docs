
### Mint NFT

{% swagger baseUrl="https://api.mintknight.com/" method="POST" path="nfts/mint" summary="Mint a NFT" %} {% swagger-description %} Mint a NFT {% endswagger-description %}

{% swagger-parameter in="header" name="Content-Type" required="true" type="string" %} A string indicating the media type of the resource {% endswagger-parameter %}

{% swagger-parameter in="header" name="x-api-key" required="true" type="string" %} Authentication token {% endswagger-parameter %}

{% swagger-parameter in="body" name="walletId" required="true" type="string" %} The wallet id to transfer the NFT {% endswagger-parameter %}

{% swagger-parameter in="body" name="metadata" required="true" type="string" %} The .... {% endswagger-parameter %}

{% swagger-response status="200" description="User successfully created" %}
{
    "collectionId": "xxx",
    "walletId": "xxxx",
    "skey": "xxxxxxx",
    "nft": nfts[0]

}


{% endswagger-response %}



{% swagger-response status="401" description="Permission denied" %}

{% endswagger-response %} {% endswagger %}



{% tabs %}
{% tab title="Node" %}
```javascript

  // Mint a NFT
  let nft = await mintknight.mintNFT(
      Contract_id,
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
