### Add drops

{% swagger baseUrl="https://api.mintknight.com/" method="POST" path="drops/" summary="Create a drop" %} {% swagger-description %} Create a drop{% endswagger-description %}

{% swagger-parameter in="header" name="Content-Type" required="true" type="string" %} A string indicating the media type of the resource {% endswagger-parameter %}

{% swagger-parameter in="header" name="x-api-key" required="true" type="string" %} Authentication token {% endswagger-parameter %}

{% swagger-parameter in="body" name="name" required="true" type="string" %}  {% endswagger-parameter %}

{% swagger-parameter in="body" name="contractId" required="true" type="string" %}  {% endswagger-parameter %}

{% swagger-parameter in="body" name="dropType" required="true" type="string" %}  {% endswagger-parameter %}

{% swagger-parameter in="body" name="totalNfts" required="true" type="number" %}  {% endswagger-parameter %}

{% swagger-parameter in="body" name="maxNfts" required="true" type="number" %}  {% endswagger-parameter %}

{% swagger-parameter in="body" name="totalYield" required="true" type="number" %}  {% endswagger-parameter %}

{% swagger-parameter in="body" name="price" required="true" type="string" %}  {% endswagger-parameter %}

{% swagger-parameter in="body" name="imgBefore" required="true" type="string" %}  {% endswagger-parameter %}

{% swagger-parameter in="body" name="imgAfter" required="true" type="string" %}  {% endswagger-parameter %}

{% swagger-parameter in="body" name="walletId" required="true" type="string" %}  {% endswagger-parameter %}

{% swagger-parameter in="body" name="skey" required="true" type="string" %}  {% endswagger-parameter %}



{
   
}
{% endswagger-response %}

{% swagger-response status="401" description="Permission denied" %}

{% endswagger-response %} {% endswagger %}