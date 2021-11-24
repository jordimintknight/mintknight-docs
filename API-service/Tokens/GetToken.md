
### Get Information of the token.

{% swagger baseUrl="https://serviceapi.mintknight.com/" method="get" path="tokens/:contractId" summary="Get Information of the token." %} {% swagger-description %} Get Information of the token. {% endswagger-description %}

{% swagger-parameter in="body" name="User_Id" required="true" type="string" %} The id of the user adding a wallet {% endswagger-parameter %}


{% swagger-response status="200" description="Token succesfully minted" %}

{

}
{% endswagger-response %}

{% swagger-response status="401" description="Permission denied" %}

{% endswagger-response %} {% endswagger %}