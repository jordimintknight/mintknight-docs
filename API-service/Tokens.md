## Tokens





### Mint Token

@return the task

{% swagger baseUrl="https://serviceapi.mintknight.com/" method="POST" path="tokens" summary="Mints a Token." %} {% swagger-description %} mints a token. {% endswagger-description %}

{% swagger-parameter in="body" name="User_Id" required="true" type="string" %} The id of the user adding a wallet {% endswagger-parameter %}


{% swagger-response status="200" description="Token succesfully minted" %}

{

}
{% endswagger-response %}

{% swagger-response status="401" description="Permission denied" %}

{% endswagger-response %} {% endswagger %}



```javascript


  // 2. Mint 50 tokens to wallet 1.
  task = await mintknight.mintToken(
    project.tokenId,
    minter.walletId,
    minter.skey,
	wallet1.walletId,
	'50',
  );
 

```


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


### Get Information of the token.

{% swagger baseUrl="https://serviceapi.mintknight.com/" method="get" path="tokens/:contractId" summary="Get Information of the token." %} {% swagger-description %} Get Information of the token. {% endswagger-description %}

{% swagger-parameter in="body" name="User_Id" required="true" type="string" %} The id of the user adding a wallet {% endswagger-parameter %}


{% swagger-response status="200" description="Token succesfully minted" %}

{

}
{% endswagger-response %}

{% swagger-response status="401" description="Permission denied" %}

{% endswagger-response %} {% endswagger %}