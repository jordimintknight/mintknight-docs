# Users

To have access to the mintknight platform, the first thing you have to do is to create a User.
To create a new User you need to make a POST request to our registration endpoint and pass the following json key-values:

```javascript
 POST https://webapi.mintknight.com/users/register
 Data: {
            "username": "your username", 
            "email": "your email", 
            "password": "your password",
            "telephone": "your telephone number"
        }

```


### Register Endpoint

{% swagger baseUrl="https://webapi.mintknight.com/" method="post" path="users/register" summary="Create User." %} {% swagger-description %} Creates a new User. {% endswagger-description %}

{% swagger-parameter in="body" name="username" required="true" type="string" %} The username of the user {% endswagger-parameter %}

{% swagger-parameter in="body" name="email" required="true" type="string" %} The email of the User {% endswagger-parameter %}

{% swagger-parameter in="body" name="password" required="true" type="string" %} The password of the user {% endswagger-parameter %}

{% swagger-parameter in="body" name="telephone" required="true" type="string" %} The phone of the user {% endswagger-parameter %}

{% swagger-response status="200" description="User successfully created" %}

{
    "role": "user",
    "updatedAt": null,
    "_id": "xxxxxxx",
    "email": "test@mail.com",
    "telephone": "2222222222",    
    "createdAt": "2021-11-05T04:10:17.851Z",
    "__v": 0,
    "token": "bearer token",
    "expiresIn": "futur date"


}
{% endswagger-response %}

{% swagger-response status="401" description="Permission denied" %}

{% endswagger-response %} {% endswagger %}


alternatively, you can create a new user by using the mintknight sdk: 

```javascript
const MintknightWeb = require('mintknight-web');

const user = await MintknightWeb.addUser(email, password, phone);

```

### Login Endpoint

Once you have Registered with our service, then you will be able to log in as admin and get the user API KEY. To log in, you have to provide your email and password used during the registration process. The log in function returns the bearer Token to use during the authentification process and the userId

{% swagger baseUrl="https://webapi.mintknight.com/" method="post" path="users/login" summary="Login " %} {% swagger-description %} Logs in a new User, return the token {% endswagger-description %}

{% swagger-parameter in="body" name="email" required="true" type="string" %} The email of the user {% endswagger-parameter %}

{% swagger-parameter in="body" name="password" required="true" type="string" %} The

password of the user {% endswagger-parameter %}

{% swagger-response status="200" description="User successfully created" %}

{
    "token": "XXXXX....XXXX",
    "userId": "XXXX........XXX"
    
}
{% endswagger-response %}

{% swagger-response status="401" description="Permission denied" %}

{% endswagger-response %} {% endswagger %}


```javascript
const MintknightWeb = require('mintknight-web');

let result = await MintknightWeb.loginUser(email, password);
```
### Get user

Returns all the information about the logged in user

{% swagger baseUrl="https://webapi.mintknight.com/" method="get" path="users/" summary="get User." %} {% swagger-description %} get User info. {% endswagger-description %}

{% swagger-parameter in="body" name="token" required="true" type="string" %} you have to pass a bearer token in the header for authentification {% endswagger-parameter %}

{% swagger-response status="200" description="User successfully created" %}

{
    "role": "user",
    "updatedAt": null,
    "_id": "xxxxxx",
    "username": "your username",
    "email": "your email",
    "telephone": "your telephone",
    "createdAt": "your creation date",
    "__v": 0
}
{% endswagger-response %}

{% swagger-response status="401" description="Permission denied" %}

{% endswagger-response %} {% endswagger %}


```javascript
const MintknightWeb = require('mintknight-web')

let result = await MintknightWeb.getUser(userId);
```
















