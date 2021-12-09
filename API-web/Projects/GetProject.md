### GET Project

This call returns all the info for a specific Project

{% swagger baseUrl="https://webapi.mintknight.com/" method="GET" path="projects/:projectId" summary="fetch a project" %} {% swagger-description %} fetch a project. {% endswagger-description %}

{% swagger-parameter in="header" name="Content-Type" required="true" type="string" %} A string indicating the media type of the resource {% endswagger-parameter %}

{% swagger-parameter in="header" name="x-api-key" required="true" type="string" %} Authentication token {% endswagger-parameter %}

{% swagger-parameter in="header" name="Content-Type" required="true" type="string" %} A string indicating the media type of the resource {% endswagger-parameter %}

{% swagger-parameter in="header" name="x-api-key" required="true" type="string" %} Authentication token {% endswagger-parameter %}

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