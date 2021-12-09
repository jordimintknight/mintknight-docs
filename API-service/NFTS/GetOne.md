
### Get one NFT

{% swagger baseUrl="https://api.mintknight.com/" method="GET" path="nfts/:contractId/:tokenId" summary="Get One NFT" %} {% swagger-description %} Get One NFT {% endswagger-description %}

{% swagger-parameter in="header" name="Content-Type" required="true" type="string" %} A string indicating the media type of the resource {% endswagger-parameter %}

{% swagger-parameter in="header" name="x-api-key" required="true" type="string" %} Authentication token {% endswagger-parameter %}

{% swagger-parameter in="body" name="name" required="true" type="string" %} The .... {% endswagger-parameter %}


{
   
}

{% endswagger-response %}

{% swagger-response status="401" description="Permission denied" %}

{% endswagger-response %} {% endswagger %}



  getNFT(contractId) {
    return this.apiCall('GET', `nfts/${contractId}`, {}, 'tokenAuth');
  }



{% tabs %}
{% tab title="Node" %}
```javascript

  // GET a NFT
  let contract = await mintknight.getNFT(
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