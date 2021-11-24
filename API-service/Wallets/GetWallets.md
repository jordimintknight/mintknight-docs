### Get Wallet info (NFTS + tokens)


@return a Wallet object

{% swagger baseUrl="https://serviceapi.mintknight.com/" method="get" path="wallets/:walletId" summary="Get one wallet and its content - nfts and tokens" %} {% swagger-description %} Get one wallet and its content - nfts and tokens. {% endswagger-description %}

{% swagger-parameter in="body" name="walletId" required="true" type="string" %} The id of the wallet {% endswagger-parameter %}

{% swagger-parameter in="body" name="network" required="true" type="string" %} the network {% endswagger-parameter %}

{% swagger-parameter in="body" name="adress" required="true" type="string" %} The adressof the wallet {% endswagger-parameter %}




{% swagger-response status="200" description="Wallet successfully added" %}

{

}
{% endswagger-response %}

{% swagger-response status="401" description="Permission denied" %}

{% endswagger-response %} {% endswagger %}