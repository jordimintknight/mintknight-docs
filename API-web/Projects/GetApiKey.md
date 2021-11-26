
### GET API KEY

{% swagger baseUrl="https://webapi.mintknight.com/" method="get" path="projects/apikey/:projectId" summary="fetch projects" %} {% swagger-description %} fetch projects. {% endswagger-description %}


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

