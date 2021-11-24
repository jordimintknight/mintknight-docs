## Nfts

```javascript
   const NFT= {
      contractId,
      *walletId,
      tokenId,
      nftType,
      title,
      description,
      image,
      attributes,
      *metadata
    };

```

### Upload NFT

{% swagger baseUrl="https://api.mintknight.com/" method="POST" path="nfts/upload" summary="Uploads a NFT" %} {% swagger-description %} Updates a NFT {% endswagger-description %}

{% swagger-parameter in="body" name="name" required="true" type="string" %} The name of the contract {% endswagger-parameter %}


{
   
}
{% endswagger-response %}

{% swagger-response status="401" description="Permission denied" %}

{% endswagger-response %} {% endswagger %}




### Mint NFT

{% swagger baseUrl="https://api.mintknight.com/" method="POST" path="nfts/mint" summary="Mint a NFT" %} {% swagger-description %} Mint a NFT {% endswagger-description %}

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



### Transfer one NFT

{% swagger baseUrl="https://api.mintknight.com/" method="PUT" path="nfts" summary="Transfer a NFT" %} {% swagger-description %} Transfer a NFT {% endswagger-description %}

{% swagger-parameter in="body" name="name" required="true" type="string" %} The .... {% endswagger-parameter %}


{
   
}
{% endswagger-response %}

{% swagger-response status="401" description="Permission denied" %}

{% endswagger-response %} {% endswagger %}


### Update NFT

{% swagger baseUrl="https://api.mintknight.com/" method="PUT" path="nfts/:nftId" summary="Updates the metadata and status of One NFT" %} {% swagger-description %} Updates the metadata and status of One NFT {% endswagger-description %}

{% swagger-parameter in="body" name="name" required="true" type="string" %} The .... {% endswagger-parameter %}


{
   
}
{% endswagger-response %}

{% swagger-response status="401" description="Permission denied" %}

{% endswagger-response %} {% endswagger %}

### Get NFT by id

{% swagger baseUrl="https://api.mintknight.com/" method="GET" path="nfts/:nftId" summary="Get one NFT by Id" %} {% swagger-description %} Get one NFT by Id {% endswagger-description %}

{% swagger-parameter in="body" name="nftId" required="true" type="string" %}  {% endswagger-parameter %}


{
   
}
{% endswagger-response %}

{% swagger-response status="401" description="Permission denied" %}

{% endswagger-response %} {% endswagger %}




### Get one NFT

{% swagger baseUrl="https://api.mintknight.com/" method="GET" path="nfts/:contractId/:tokenId" summary="Get One NFT" %} {% swagger-description %} Get One NFT {% endswagger-description %}

{% swagger-parameter in="body" name="name" required="true" type="string" %} The .... {% endswagger-parameter %}


{
   
}

{% endswagger-response %}

{% swagger-response status="401" description="Permission denied" %}

{% endswagger-response %} {% endswagger %}
