
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


  mintToken(contractId, walletId, skey, to, value) 
  uploadImage(imageFile)

{% tabs %}
{% tab title="Node" %}
```javascript

  // Mint a token
  let token = await mintknight.mintToken(
      Contract_id,
      walletId,
      skey,
      to,
      value      
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