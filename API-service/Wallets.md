## Wallets

```javascript

const Wallet = {
      projectId,
      companyId,
      *UserRef
      type:
      address,
      owner,
      network,
      *skey,
      userId,
      
    });

```

### Add Wallet 
@return a Wallet object

{% swagger baseUrl="https://serviceapi.mintknight.com/" method="post" path="wallets" summary="Deploy a new wallet" %} {% swagger-description %} Deploys a new wallet. {% endswagger-description %}

{% swagger-parameter in="body" name="companyId" required="true" type="string" %} The id of the company adding a wallet {% endswagger-parameter %}

{% swagger-parameter in="body" name="owner" required="true" type="string" %} The id of the user adding a wallet {% endswagger-parameter %}

{% swagger-parameter in="body" name="network" required="true" type="string" %} The id of the user adding a wallet {% endswagger-parameter %}

{% swagger-parameter in="body" name="skey" required="true" type="string" %} The id of the user adding a wallet {% endswagger-parameter %}

{% swagger-parameter in="body" name="refUser" required="true" type="string" %} The id of the user adding a wallet {% endswagger-parameter %}

{% swagger-response status="200" description="Wallet successfully added" %}

{

}
{% endswagger-response %}

{% swagger-response status="401" description="Permission denied" %}

{% endswagger-response %} {% endswagger %}




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