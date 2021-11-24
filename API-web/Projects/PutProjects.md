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