
### Transfer Token

@return Token Info

{% swagger baseUrl="https://serviceapi.mintknight.com/" method="PUT" path="tokens" summary="Transfer a Token." %} {% swagger-description %} transfer a token. {% endswagger-description %}

{% swagger-parameter in="header" name="Content-Type" required="true" type="string" %} A string indicating the media type of the resource {% endswagger-parameter %}

{% swagger-parameter in="header" name="x-api-key" required="true" type="string" %} Authentication token {% endswagger-parameter %}

{% swagger-parameter in="body" name="User_Id" required="true" type="string" %} The id of the user adding a wallet {% endswagger-parameter %}


{% swagger-response status="200" description="Token succesfully minted" %}

{

}
{% endswagger-response %}

{% swagger-response status="401" description="Permission denied" %}

{% endswagger-response %} {% endswagger %}


{% tabs %}
{% tab title="Node" %}
```javascript
  // 3. Transfer 10 tokens to Wallet2.
  task = await mintknight.transferToken(
    project.contractId,
    wallet1.walletId,
    wallet1.skey,
    wallet2.walletId,
    '10');
  task = await mintknight.waitTask(task.taskId);
```
{% endtab %}

{% tab title="Python" %}
```
# Install via pip
pip install --upgrade myapi
```
{% endtab %}
{% endtabs %}



