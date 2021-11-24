## Projects

Projects helps to organize your collections, drops, NFT. 
Only authentificated users can create and manage projects.
As an example, for a marketing agency, projects could be the different brands that represents.  

The project object have the following structure:

```javascript
 Data: {
            "name": "your Project Name ", 
            "description": "the description of the project", 
            "network": "your network choice"
            
        }
```


### POST Projects

This action creats a new project for the user. The json key values that are required to create a project are the following:


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


```javascript
  const MintknightWeb = require('mintknight-web');
  
  const project = await Mintknight.addProject(
    PROJECT_NAME,
    PROJECT_DESCRIPTION,
    PROJECT_NETWORK
  );
```
### GET Projects
This call returns an object with the total number of projects for the user and an array of projects with a project object for each project

{% swagger baseUrl="https://webapi.mintknight.com/" method="GET" path="projects" summary="fetch projects" %} {% swagger-description %} fetch projects. {% endswagger-description %}


{% swagger-response status="200" description="Projects successfully fetched" %}

{
    "total": 1,
    "projects": [
        {
            "_id": "6184bffffd95930012b9a39d",
            "name": "Test projectCompany",
            "description": "this is a description",
            "network": "mumbai",
            "createdAt": "2021-11-05T05:24:15.026Z",
            "updatedAt": "2021-11-05T05:24:15.026Z",
            "companyId": "6184b57e7771000019c8de34",
            "createdBy": "6184aea9fd95930012b9a39c",
            "__v": 0
        }
    ]
}
{% endswagger-response %}

{% swagger-response status="401" description="Permission denied" %}

{% endswagger-response %} {% endswagger %}



### GET Project

This call returns all the info for a specific Project

{% swagger baseUrl="https://webapi.mintknight.com/" method="GET" path="projects/:projectId" summary="fetch a project" %} {% swagger-description %} fetch a project. {% endswagger-description %}


{% swagger-response status="200" description="Projects successfully fetched" %}

        {
            "_id": "6184bffffd95930012b9a39d",
            "name": "Test projectCompany",
            "description": "this is a description",
            "network": "mumbai",
            "createdAt": "2021-11-05T05:24:15.026Z",
            "updatedAt": "2021-11-05T05:24:15.026Z",
            "companyId": "6184b57e7771000019c8de34",
            "createdBy": "6184aea9fd95930012b9a39c",
            "__v": 0
        }

{% endswagger-response %}

{% swagger-response status="401" description="Permission denied" %}

{% endswagger-response %} {% endswagger %}


```javascript
const MintknightWeb = require('mintknight-web');

let ProjectInfo = static async Mintknight.getProject(user, projectId) 
```


### PUT Project


{% swagger baseUrl="https://webapi.mintknight.com/" method="PUT" path="projects/:projectId" summary="Update project" %} {% swagger-description %} fetch a project. {% endswagger-description %}

{% swagger-parameter in="body" name="name" required="true" type="string" %} The name of the project {% endswagger-parameter %}

{% swagger-parameter in="body" name="description" required="true" type="string" %} The description of the Project {% endswagger-parameter %}

{% swagger-parameter in="body" name="network" required="true" type="string" %} The network used in this project {% endswagger-parameter %}

{% swagger-response status="200" description="Projects successfully fetched" %}

        {
            "_id": "6184bffffd95930012b9a39d",
            "name": "Test projectCompany",
            "description": "this is a description",
            "network": "mumbai",
            "createdAt": "2021-11-05T05:24:15.026Z",
            "updatedAt": "2021-11-05T05:24:15.026Z",
            "companyId": "6184b57e7771000019c8de34",
            "createdBy": "6184aea9fd95930012b9a39c",
            "__v": 0
        }

{% endswagger-response %}

{% swagger-response status="401" description="Permission denied" %}

{% endswagger-response %} {% endswagger %}


### GET API KEY

{% swagger baseUrl="https://webapi.mintknight.com/" method="get" path="projects/apikey/:projectId" summary="fetch projects" %} {% swagger-description %} fetch projects. {% endswagger-description %}


{% swagger-response status="200" description="Project API KEY successfully fetched" %}

{
    "token": "XXXXXXXXXX..XXXXXX",
   }
{% endswagger-response %}

{% swagger-response status="401" description="Permission denied" %}

{% endswagger-response %} {% endswagger %}


```javascript
 const apiKey = await mintknight.getApiKey(projectId);
```


