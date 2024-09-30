# User API Spec

## Register User API

Endpoint : POST /api/users

Request Body :

```json
{
  "username": "pzn",
  "password": "rahasia",
  "name": "Programmer Zaman Now"
}
```

Response Body :

```json
{
  "data": {
    "username": "pzn",
    "name": "Programmer Zaman Now"
  }
}
```

Response Body Error :

```json
{
  "username": "username already registered"
}
```

## Login User API

Endpoint : Post /api/users/login

Request Body :

````json
{
  "username": "pzn",
  "password": "rahasia"
}

Response Body Success :

```json
{
    "data" : {
     "token": "unique-token"
    }
}
````

Response Body Error :

```json
{
  "errors": "username and password wrong"
}
```

## Get User API

## Logout User API
