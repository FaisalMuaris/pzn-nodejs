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

## Update User API

Endpoint : PATCH /api/users/current

Headers :

- Authorization : token

Request Body :

```json
{
  "name": "Programmer Zaman Now",
  "password": "new password"
}
```

Response Body Success :

```json
{
  "data": {
    "username": "pzn",
    "name": "programmer zaman now lagi"
  }
}
```

Response Body Error :

```json
{
  "errors": "name length max 100"
}
```

## Get User API

Endpont : GET /api/users/current

Headers :

- Authorization : token

Response Body Success :

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
  "error": "Unauthorized"
}
```

## Logout User API

Endpoint : DELETE /api/users/logout

Headers :

- Authorization : token

Response Body Success :

```json
{
  "data": "OK"
}
```

Response Body Errors :

```json
{
  "errors": "Unauthorized"
}
```
