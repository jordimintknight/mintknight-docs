### POST Projects

This action creats a new project for the user. The json key values that are required to create a project are the following:



{% swagger src="https://sandbox.mintknight.com/api-docs/#/projects/post_projects.swagger.json
" path="/projects" method="put" %} https://petstore.swagger.io/v2/swagger.json {% endswagger %}


https://sandbox.mintknight.com/api-docs/#/projects/post_projects.swagger.json


{% swagger baseUrl="https://webapi.mintknight.com/" method="POST" path="projects" summary="Creats a new project" %} {% swagger-description %} Creates a new Project. {% endswagger-description %}

{% swagger-parameter in="body" name="name" required="true" type="string" %} The name of the project {% endswagger-parameter %}

{% swagger-parameter in="body" name="description" required="true" type="string" %} The description of the Project {% endswagger-parameter %}

{% swagger-parameter in="body" name="network" required="true" type="string" %} The network used in this project {% endswagger-parameter %}


{% swagger-response status="200" description="Project successfully created" %}

{
    "_id": "XXXXXXXXXXXX...XX",
    "name": "the name of a project",
    "description": "this is the project description",
    "network": "the network your project is working",
    "createdAt": "2021-11-05T05:24:15.026Z",
    "updatedAt": "2021-11-05T05:24:15.026Z",
    "companyId": "Company_ID",
    "createdBy": "User_ID",
    "__v": 0
}
{% endswagger-response %}

{% swagger-response status="401" description="Permission denied" %}

{% endswagger-response %} {% endswagger %}


{% tabs %}
{% tab title="Node" %}
```javascript
  const MintknightWeb = require('mintknight-web');
  
  const project = await Mintknight.addProject(
    PROJECT_NAME,
    PROJECT_DESCRIPTION,
    PROJECT_NETWORK
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
