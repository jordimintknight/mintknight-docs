
### Transfer Token

@return Token Info

{% swagger baseUrl="https://serviceapi.mintknight.com/" method="PUT" path="tokens" summary="Transfer a Token." %} {% swagger-description %} transfer a token. {% endswagger-description %}

{% swagger-parameter in="body" name="User_Id" required="true" type="string" %} The id of the user adding a wallet {% endswagger-parameter %}


{% swagger-response status="200" description="Token succesfully minted" %}

{

}
{% endswagger-response %}

{% swagger-response status="401" description="Permission denied" %}

{% endswagger-response %} {% endswagger %}
