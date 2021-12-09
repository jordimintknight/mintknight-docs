
### GET API KEY

{% swagger baseUrl="https://webapi.mintknight.com/" method="get" path="projects/apikey/:projectId" summary="fetch projects" %} {% swagger-description %} fetch projects. {% endswagger-description %}

{% swagger-parameter in="header" name="Content-Type" required="true" type="string" %} A string indicating the media type of the resource {% endswagger-parameter %}

{% swagger-parameter in="header" name="x-api-key" required="true" type="string" %} Authentication token {% endswagger-parameter %}

{% swagger-response status="200" description="Project API KEY successfully fetched" %}

{
    "token": "XXXXXXXXXX..XXXXXX",
   }
{% endswagger-response %}

{% swagger-response status="401" description="Permission denied" %}

{% endswagger-response %} {% endswagger %}


{% tabs %}
{% tab title="Node" %}
```javascript

const apiKey = await mintknight.getApiKey(projectId);

```
{% endtab %}

{% tab title="Python" %}
```
# Install via pip
pip install --upgrade myapi
```
{% endtab %}
{% endtabs %}

