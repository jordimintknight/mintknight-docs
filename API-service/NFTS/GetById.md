
### Get NFT by id

{% swagger baseUrl="https://api.mintknight.com/" method="GET" path="nfts/:nftId" summary="Get one NFT by Id" %} {% swagger-description %} Get one NFT by Id {% endswagger-description %}

{% swagger-parameter in="header" name="Content-Type" required="true" type="string" %} A string indicating the media type of the resource {% endswagger-parameter %}

{% swagger-parameter in="header" name="x-api-key" required="true" type="string" %} Authentication token {% endswagger-parameter %}

{% swagger-parameter in="body" name="nftId" required="true" type="string" %}  {% endswagger-parameter %}


{
   
}
{% endswagger-response %}

{% swagger-response status="401" description="Permission denied" %}

{% endswagger-response %} {% endswagger %}

