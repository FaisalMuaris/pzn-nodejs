# Contact API Spec

## Create Contact API

Endpoint : POST /api/contacts

Header :

- Authorization : token

Request Body :

```json
{
  "first_name": "Faisal",
  "last_name": "Muaris",
  "email": "faisal@gmail.com",
  "phone": "131141413"
}
```

Response Body Success:

```json
{
  "data": {
    "id": 1,
    "first_name": "Faisal",
    "last_name": "Muaris",
    "email": "faisal@gmail.com",
    "phone": "131141413"
  }
}
```

Response Body Errors:

```json
{
  "errors": "Email is not valid"
}
```

## Update Contact API

Endpoint : PUT /api/contacts/:id

Header :

- Authorization : token

Request Body :

```json
{
  "first_name": "Faisal",
  "last_name": "Muaris",
  "email": "faisal@gmail.com",
  "phone": "131141413"
}
```

Response Body Success:

```json
{
  "data": {
    "id": 1,
    "first_name": "Faisal",
    "last_name": "Muaris",
    "email": "faisal@gmail.com",
    "phone": "131141413"
  }
}
```

Response Body Errors:

```json
{
  "errors": "email is not valid"
}
```

## Get Contact API

Endpoint : GET /api/contacts/:id

Header :

- Authorization : token

Response Body Success:

```json
{
  "data": {
    "id": 1,
    "first_name": "Faisal",
    "last_name": "Muaris",
    "email": "faisal@gmail.com",
    "phone": "131141413"
  }
}
```

Response Body Errors:

```json
{
  "errors": "Contact is not found"
}
```

## Search Contact API

Endpoint : GET /api/contacts

Header :

- Authorization : token

Query Parameters :

- name : Search first_name or last_name, using like, optional
- email : Search by email, using like, optional
- phone : Search by phone number, using like, optional
- page : number of page, default 1
- size : size of page, default 10

Response Body Success:

```json
{
  "data": {
    "id": 1,
    "first_name": "Faisal",
    "last_name": "Muaris",
    "email": "faisal@gmail.com",
    "phone": "131141413"
  },
  "data": {
    "id": 2,
    "first_name": "Faisal",
    "last_name": "Muaris",
    "email": "faisal@gmail.com",
    "phone": "131141413"
  },
  "paging": 1,
  "total_page": 3,
  "total_item": 30
}
```

Response Body Errors:

## Remove Contact API

Endpoint : DELETE /api/contacts/:id

Header :

- Authorization : token

Response Body Success:

```json
{
  "data": "OK"
}
```

Response Body Errors:

```json
{
  "errors": "contact is not found"
}
```
