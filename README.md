# Social Media API
I wrote this web-services Social Media API to learn more about Spring Boot. It connects to MongoDB. 

## Features

* **_List all the users in the Database_**

> Method: `[GET]` </br>
> Endpoint: `/users` </br>
> Authentication: `None` </br>
> Query Parameters: `None` </br>

### Example responses: 

* Status Code: `[200]`

```java
[
    {
        "id": "5fd7636a7d3e0f2da15d0fb6",
        "name": "Bill Gates",
        "email": "billgates@microsoft.com"
    },
    {
        "id": "5fd7636a7d3e0f2da15d0fb7",
        "name": "Josh",
        "email": "josh@hotmail.com"
    },
    {
        "id": "5fd7636a7d3e0f2da15d0fb8",
        "name": "Jack Buffallo-Head",
        "email": "jack@gmail.com"
    }
]
```

<hr>

 * **_List a specific user by Id_**

> Method: `[GET]` </br>
> Endpoint: `/users/{id}` </br>
> Authentication: `None` </br>
> Query Parameters: `None` </br>

### Example responses: 

* Status Code: `[200]`

```java
[
    {
        "id": "5fd7636a7d3e0f2da15d0fb6",
        "name": "Bill Gates",
        "email": "billgates@microsoft.com"
    }
]
```

* Status Code: `[404 Not Found]`

```java
{
    "timestamp": 1607953495881,
    "status": 404,
    "error": "Not Found",
    "message": "User not found.",
    "path": "/users/23"
}
```
<hr>

* **_List all posts made by a specific user_**

> Method: `[GET]` </br>
> Endpoint: `/users/{id}/posts` </br>
> Authentication: `None` </br>
> Query Parameters: `None` </br>

### Example responses: 

* Status Code: `[200]`

```java
[
    {
        "id": "5fd76d1d7f7a9e7acb13162c",
        "date": "1999-02-21T00:00:00.000+00:00",
        "title": "Goodbye",
        "body": "Cruel World",
        "author": {
            "id": "5fd76d1d7f7a9e7acb131629",
            "name": "John"
        }
    },
    {
        "id": "5fd76d1d7f7a9e7acb13162d",
        "date": "1998-02-21T00:00:00.000+00:00",
        "title": "Somewhere",
        "body": "I belong!",
        "author": {
            "id": "5fd76d1d7f7a9e7acb131629",
            "name": "John"
        }
    }
]
```

