### GET Projects
This call returns an object with the total number of projects for the user and an array of projects with a project object for each project

{% swagger baseUrl="https://webapi.mintknight.com/" method="GET" path="projects" summary="fetch projects" %} {% swagger-description %} fetch projects. {% endswagger-description %}

{% swagger-parameter in="header" name="Content-Type" required="true" type="string" %} A string indicating the media type of the resource {% endswagger-parameter %}

{% swagger-parameter in="header" name="x-api-key" required="true" type="string" %} Authentication token {% endswagger-parameter %}

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