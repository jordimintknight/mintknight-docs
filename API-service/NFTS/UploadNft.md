
### Upload NFT

{% swagger baseUrl="https://api.mintknight.com/" method="POST" path="nfts/upload" summary="Uploads a NFT" %} {% swagger-description %} Updates a NFT {% endswagger-description %}

{% swagger-parameter in="body" name="name" required="true" type="string" %} The name of the contract {% endswagger-parameter %}


{
   
}
{% endswagger-response %}

{% swagger-response status="401" description="Permission denied" %}

{% endswagger-response %} {% endswagger %}



uploadImage(imageFile)

{% tabs %}
{% tab title="Node" %}
```javascript

  // Upload nft Image
  let nft = await mintknight.uploadImage(imageFile);
   
```
{% endtab %}

{% tab title="Python" %}
```
# Install via pip
pip install --upgrade myapi
```
{% endtab %}
{% endtabs %}