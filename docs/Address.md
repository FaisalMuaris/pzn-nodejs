# Address API Spec

## Create Address API

Endpoint : POST /api/contact/:contactId/addresses

Header:

- Authorization : token

Request Body :

```json
{
  "street": "Jalan apa",
  "city": "Kota apa",
  "province": "Provinsi Apa",
  "country": "Negara apa",
  "postal_code": "kode pos"
}
```

Response Body Success :

```json
{
  "data": {
    "id": 1,
    "street": "Jalan apa",
    "city": "Kota apa",
    "province": "Provinsi Apa",
    "country": "Negara apa",
    "postal_code": "kode pos"
  }
}
```

Response Body Error :

```json
{
  "error": "Country is required"
}
```

## Update Address API

Endpoint : PUT /api/contact/:contactId/addresses/:addressId

Header:

- Authorization : token

Request Body :

```json
{
  "street": "Jalan apa",
  "city": "Kota apa",
  "province": "Provinsi Apa",
  "country": "Negara apa",
  "postal_code": "kode pos"
}
```

Response Body Success :

```json
{
  "data": {
    "id": 1,
    "street": "Jalan apa",
    "city": "Kota apa",
    "province": "Provinsi Apa",
    "country": "Negara apa",
    "postal_code": "kode pos"
  }
}
```

Response Body Error :

```json
{
  "error": "Country is required"
}
```

## Get Address API

Endpoint : GET /api/contact/:contactId/addresses/:addressId

Header:

- Authorization : token

Response Body Success :

```json
{
  "data": {
    "id": 1,
    "street": "Jalan apa",
    "city": "Kota apa",
    "province": "Provinsi Apa",
    "country": "Negara apa",
    "postal_code": "kode pos"
  }
}
```

Response Body Error :

```json
{
  "error": "Contact is not found"
}
```

## List Addresses API

Endpoint : GET /api/contact/:contactId/addresses

Header:

- Authorization : token

Response Body Success :

```json
{
  "data": [
    {
      "id": 1,
      "street": "Jalan apa",
      "city": "Kota apa",
      "province": "Provinsi Apa",
      "country": "Negara apa",
      "postal_code": "kode pos"
    },
    {
      "id": 2,
      "street": "Jalan apa",
      "city": "Kota apa",
      "province": "Provinsi Apa",
      "country": "Negara apa",
      "postal_code": "kode pos"
    }
  ]
}
```

Response Body Error :

```json
{
  "error": "Contact is not found"
}
```

## Remove Address API

Endpoint : DELETE /api/contactId/:contactId/addresses/:addressId

Header:

- Authorization : token

Response Body Success :

```json
{
  "data": "OK"
}
```

Response Body Error :

```json
{
  "error": "Address is not found"
}
```
