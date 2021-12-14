### POST Projects

This action creats a new project for the user. The json key values that are required to create a project are the following:


{% swagger baseUrl="https://webapi.mintknight.com/" method="POST" path="mails" summary="sending an email" %} {% swagger-description %} sends an email {% endswagger-description %}


{% swagger-parameter in="header" name="Content-Type" required="true" type="string" %} A string indicating the media type of the resource {% endswagger-parameter %}

{% swagger-parameter in="header" name="x-api-key" required="true" type="string" %} Authentication token {% endswagger-parameter %}


{% swagger-parameter in="body" name="" required="true" type="string" %} The name of the project {% endswagger-parameter %}

{% swagger-parameter in="body" name="description" required="true" type="string" %} The description of the Project {% endswagger-parameter %}

{% swagger-parameter in="body" name="network" required="true" type="string" %} The network used in this project {% endswagger-parameter %}


{% swagger-response status="200" description="Project successfully created" %}


}
{% endswagger-response %}

{% swagger-response status="401" description="Permission denied" %}

{% endswagger-response %} {% endswagger %}
