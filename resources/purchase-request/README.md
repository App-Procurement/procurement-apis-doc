# Purchase Request

This object represents the Purchase Requests that is raised from the internal employees of the organization to purchase any item.

**EndPoints**

    GET api/v1/requests

    POST api/v1/requests

    POST api/v1/requests/:id

    DELETE api/v1/requests/:id 

    POST api/v1/requests/approve/:id

    POST api/v1/requests/deactivate/:id

    GET api/v1/requests/search

## The Purchase Request Object

**Attributes**

|name|type|description|
|---|---|---|
|id| long|Unique identifier for the object.|
|details| jsonb| Details for the object.|

/papu --pls describe the jsonb fields

**The Object**

```json    
{
    "createdBy": "Jitin",
    "createdOn": "01-01-2022",
    "updatedBy": "updater name",
    "updatedOn": "01-01-2022",
    "approvedBy": "approverId",
    "approvedOn": "01-01-2022",
    "desiredDate": "01-01-2022",
    "location": "head office",
    "requestType": "purchase",
    "note": "mahaveer",
    "state": "pending",
    "progressStage": "new",
    "totalAmount": 824,
    "department": "development",
    "document": [
        {
            "name": "name",
            "url": ""
        },
        {
            "name": "name",
            "url": ""
        },
        {
            "name": "name",
            "url": ""
        }
    ],
    "products": [
        {
            "item": {
                "id": 3,
                "itemName": "mouse",
                "itemType": "product",
                "unit": "each",
                "category": "tech",
                "price": 12,
                "supplier": {
                    "id": 2,
                    "name": "raghav das",
                    "email": "this@gmail.com",
                    "contact": "+91 9876543210",
                    "telephoneNo": "012-65432",
                    "designationNo": "1233",
                    "automateSending": "true",
                    "city": "jaipur",
                    "state": "rajasthan",
                    "postalCode": "13468",
                    "country": "USA",
                    "paymentTerms": "terms",
                    "category": "cat",
                    "address": "Street no. B6, Miami",
                    "status": "active",
                    "company": {
                        "name": "flipkart",
                        "registrationNo": "123"
                    },
                    "bankDetails": {
                        "accountHolderName": "jitin",
                        "accountNo": "1234565789",
                        "bank": "ABCD",
                        "taxId": "DFS55465dFS",
                        "currency": {
                            "id": 1,
                            "code": "USD",
                            "name": "doller",
                            "countryName": "USA",
                            "countryCode": 1
                        }
                    },
                    "document": [
                        {
                            "name": "name",
                            "url": ""
                        },
                        {
                            "name": "name",
                            "url": ""
                        },
                        {
                            "name": "name",
                            "url": ""
                        }
                    ]
                }
            },
            "quantity": 1
        },
        {
            "item": {
                "id": 2,
                "itemName": "hp laptop",
                "itemType": "product",
                "unit": "each",
                "category": "tech",
                "price": 800,
                "supplier": {
                    "id": 1,
                    "name": "andrew choudhary",
                    "email": "this@gmail.com",
                    "contact": "+91 9876543210",
                    "telephoneNo": "012-65432",
                    "designationNo": "1233",
                    "automateSending": "true",
                    "city": "jaipur",
                    "state": "rajasthan",
                    "postalCode": "13468",
                    "country": "USA",
                    "paymentTerms": "terms",
                    "category": "cat",
                    "address": "Street no. B6, Miami",
                    "status": "active",
                    "company": {
                        "name": "amazone",
                        "registrationNo": "123"
                    },
                    "bankDetails": {
                        "accountHolderName": "jitin",
                        "accountNo": "1234565789",
                        "bank": "ABCD",
                        "taxId": "DFS55465dFS",
                        "currency": {
                            "id": 1,
                            "code": "USD",
                            "name": "doller",
                            "countryName": "USA",
                            "countryCode": 1
                        }
                    },
                    "document": [
                        {
                            "name": "name",
                            "url": ""
                        },
                        {
                            "name": "name",
                            "url": ""
                        },
                        {
                            "name": "name",
                            "url": ""
                        }
                    ]
                }
            },
            "quantity": 1
        }
    ]
}
```

## Create a Purchase Request

**Description**

Create a purchase request object.

**Parameters**

|name|type|description|
|---|---|---|
|id| long|Unique identifier for the object.|
|details| jsonb| Details for the object.|

**Return**

Returns the success status if the update succeeded. Returns an error if create parameters are invalid (e.g. specifying an invalid coupon or an invalid source).

**Curl Request**

    curl https://api.stripe.com/v1/customers \
    -u sk_test_4eC39HqLyjWDarjtT1zdp7dc: \
    -d description="My First Test Customer (created for API docs at https://www.stripe.com/docs/api)"

**Response**

```json   
{
    "code": 200,
    "message": "request added successfully",
    "type": "object",
    "object": []
}
```

## Update a Purchase Request

**Description**

Update a purchase request object.

**Parameters**

|name|type|description|
|---|---|---|
|id| long|Unique identifier for the object.|
|details| jsonb| Details for the object.|

**Return**

Returns the success status if the update succeeded. Returns an error if create parameters are invalid (e.g. specifying an invalid coupon or an invalid source).

**Curl Request**

    curl https://api.stripe.com/v1/customers \
    -u sk_test_4eC39HqLyjWDarjtT1zdp7dc: \
    -d description="My First Test Customer (created for API docs at https://www.stripe.com/docs/api)"

**Response**

```json   
{
    "code": 200,
    "message": "request updated successfully",
    "type": "object",
    "object": []
}
```

## Delete a Purchase Request

**Description**

Delete a purchase request object.

**Parameters**

|name|type|description|
|---|---|---|
|id| long|Unique identifier for the object.|
|details| jsonb| Details for the object.|

**Return**

Returns the success status if the update succeeded. Returns an error if create parameters are invalid (e.g. specifying an invalid coupon or an invalid source).

**Curl Request**

    curl https://api.stripe.com/v1/customers \
    -u sk_test_4eC39HqLyjWDarjtT1zdp7dc: \
    -d description="My First Test Customer (created for API docs at https://www.stripe.com/docs/api)"

**Response**

```json   
{
    "code": 200,
    "message": "request deleted successfully",
    "type": "object",
    "object": []
}
```

## Approve a Purchase Request

**Description**

Approve a purchase request object.

**Parameters**

|name|type|description|
|---|---|---|
|id| long|Unique identifier for the object.|
|details| jsonb| Details for the object.|

**Return**

Returns the success status if the update succeeded. Returns an error if create parameters are invalid (e.g. specifying an invalid coupon or an invalid source).

**Curl Request**

    curl https://api.stripe.com/v1/customers \
    -u sk_test_4eC39HqLyjWDarjtT1zdp7dc: \
    -d description="My First Test Customer (created for API docs at https://www.stripe.com/docs/api)"

**Response**

```json   
{
    "code": 200,
    "message": "request approved successfully",
    "type": "object",
    "object": []
}
```

## Deactivate a Purchase Request

**Description**

Deactivate a purchase request object.

**Parameters**

|name|type|description|
|---|---|---|
|id| long|Unique identifier for the object.|
|details| jsonb| Details for the object.|

**Return**

Returns the success status if the update succeeded. Returns an error if create parameters are invalid (e.g. specifying an invalid coupon or an invalid source).

**Curl Request**

    curl https://api.stripe.com/v1/customers \
    -u sk_test_4eC39HqLyjWDarjtT1zdp7dc: \
    -d description="My First Test Customer (created for API docs at https://www.stripe.com/docs/api)"

**Response**

```json   
{
    "code": 200,
    "message": "request deactivated successfully",
    "type": "object",
    "object": []
}
```

## Search Purchase Requests

**Description**

Search a purchase request object.

**Parameters**

|name|type|description|
|---|---|---|
|id| long|Unique identifier for the object.|
|details| jsonb| Details for the object.|

**Return**

Returns the success status if the update succeeded. Returns an error if create parameters are invalid (e.g. specifying an invalid coupon or an invalid source).

**Curl Request**

    curl https://api.stripe.com/v1/customers \
    -u sk_test_4eC39HqLyjWDarjtT1zdp7dc: \
    -d description="My First Test Customer (created for API docs at https://www.stripe.com/docs/api)"

**Response**

```json   
{
    "code": 200,
    "message": "request search successfully",
    "type": "object",
    "object": [*Array of resultant objects*]
}
```

#  Product

This object represents the Products that is raised from the internal employees of the organization to any item.

**EndPoints**

    POST {{baseUrl}}/product

    PUT {{baseUrl}}/product/:id
    
    DELETE {{baseUrl}}/product/:id

    POST {{baseUrl}}/product/deactivate/:id

    GET {{baseUrl}}/product

## The Product Object

**Attributes**

|name|type|description|
|---|---|---|
|id| long|Unique identifier for the object.|
|details| jsonb| Details for the object.|

**The Object**

```json    
{
        "itemName": "hp laptop",
        "itemType": "product",
        "unit": "each",
        "category": "tech",
        "price": 800,
        "imgUrl": "http://imgSynectiks.com",
        "supplier": {
            "id": 1,
            "name": "andrew choudhary",
            "email": "this@gmail.com",
            "contact": "+91 9876543210",
            "telephoneNo": "012-65432",
            "designationNo": "1233",
            "automateSending": "true",
            "city": "jaipur",
            "state": "rajasthan",
            "postalCode": "13468",
            "country": "USA",
            "paymentTerms": "terms",
            "category": "cat",
            "address": "Street no. B6, Miami",
            "status": "active",
            "company": {
                "name": "amazone",
                "registrationNo": "123"
            },
            "bankDetails": {
                "accountHolderName": "jitin",
                "accountNo": "1234565789",
                "bank": "ABCD",
                "taxId": "DFS55465dFS",
                "currency": {
                    "id": 1,
                    "code": "USD",
                    "name": "doller",
                    "countryName": "USA",
                    "countryCode": 1
                }
            },
            "document": [
                {
                    "name": "name",
                    "url": ""
                },
                {
                    "name": "name",
                    "url": ""
                },
                {
                    "name": "name",
                    "url": ""
                }
            ]
        }
    }
```

## Create a Product

**Description**

Create a product object.

**Parameters**

|name|type|description|
|---|---|---|
|id| long|Unique identifier for the object.|
|details| jsonb| Details for the object.|

**Return**

Returns the success status if the update succeeded. Returns an error if create parameters are invalid (e.g. specifying an invalid coupon or an invalid source).

**Curl Request**

    curl https://api.stripe.com/v1/customers \
    -u sk_test_4eC39HqLyjWDarjtT1zdp7dc: \
    -d description="My First Test Customer (created for API docs at https://www.stripe.com/docs/api)"

**Response**

```json   
{
    "code": 200,
    "message": "product added successfully",
    "type": "object",
    "object": []
}
```

## Update a Product

**Description**

Update a product object.

**Parameters**

|name|type|description|
|---|---|---|
|id| long|Unique identifier for the object.|
|details| jsonb| Details for the object.|

**Return**

Returns the success status if the update succeeded. Returns an error if create parameters are invalid (e.g. specifying an invalid coupon or an invalid source).

**Curl Request**

    curl https://api.stripe.com/v1/customers \
    -u sk_test_4eC39HqLyjWDarjtT1zdp7dc: \
    -d description="My First Test Customer (created for API docs at https://www.stripe.com/docs/api)"

**Response**

```json   
{
    "code": 200,
    "message": "product updated successfully",
    "type": "object",
    "object": []
}
```

## Delete a Product

**Description**

Delete a product object.

**Parameters**

|name|type|description|
|---|---|---|
|id| long|Unique identifier for the object.|
|details| jsonb| Details for the object.|

**Return**

Returns the success status if the update succeeded. Returns an error if create parameters are invalid (e.g. specifying an invalid coupon or an invalid source).

**Curl Request**

    curl https://api.stripe.com/v1/customers \
    -u sk_test_4eC39HqLyjWDarjtT1zdp7dc: \
    -d description="My First Test Customer (created for API docs at https://www.stripe.com/docs/api)"

**Response**

```json   
{
    "code": 200,
    "message": "product deleted successfully",
    "type": "object",
    "object": []
}
```

## Deactivate a Product

**Description**

Deactivate a product object.

**Parameters**

|name|type|description|
|---|---|---|
|id| long|Unique identifier for the object.|
|details| jsonb| Details for the object.|

**Return**

Returns the success status if the update succeeded. Returns an error if create parameters are invalid (e.g. specifying an invalid coupon or an invalid source).

**Curl Request**

    curl https://api.stripe.com/v1/customers \
    -u sk_test_4eC39HqLyjWDarjtT1zdp7dc: \
    -d description="My First Test Customer (created for API docs at https://www.stripe.com/docs/api)"

**Response**

```json   
{
    "code": 200,
    "message": "product deactivated successfully",
    "type": "object",
    "object": []
}
```

## Search Product

**Description**

Search a product object.

**Parameters**

|name|type|description|
|---|---|---|
|id| long|Unique identifier for the object.|
|details| jsonb| Details for the object.|

**Return**

Returns the success status if the update succeeded. Returns an error if create parameters are invalid (e.g. specifying an invalid coupon or an invalid source).

**Curl Request**

    curl https://api.stripe.com/v1/customers \
    -u sk_test_4eC39HqLyjWDarjtT1zdp7dc: \
    -d description="My First Test Customer (created for API docs at https://www.stripe.com/docs/api)"

**Response**

```json   
{
    "code": 200,
    "message": "product search successfully",
    "type": "object",
    "object": [*Array of resultant objects*]
}
```

# Supplier

This object represents the Supplier that is raised from the internal employees of the organization to any item.

**EndPoints**

    POST {{baseUrl}}/supplier

    PUT {{baseUrl}}/supplier/:id
    
    DELETE {{baseUrl}}/supplier/:id

    POST {{baseUrl}}/supplier/deactivate

    GET {{baseUrl}}/supplier

## The Supplier Object

**Attributes**

|name|type|description|
|---|---|---|
|id| long|Unique identifier for the object.|
|details| jsonb| Details for the object.|

**The Object**

```json 
   {
        "name": "raghav das",
        "email": "this@gmail.com",
        "contact": "+91 9876543210",
        "telephoneNo": "012-65432",
        "designationNo": "1233",
        "automateSending": "true",
        "city": "jaipur",
        "state": "rajasthan",
        "postalCode": "13468",
        "country": "USA",
        "paymentTerms": "terms",
        "category": "cat",
        "address": "Street no. B6, Miami",
        "status": "active",
        "company": {
            "name": "flipkart",
            "registrationNo": "123"
        },
        "bankDetails": {
            "accountHolderName": "jitin",
            "accountNo": "1234565789",
            "bank": "ABCD",
            "taxId": "DFS55465dFS",
            "currency": {
                "id": 1,
                "code": "USD",
                "name": "doller",
                "countryName": "USA",
                "countryCode": 1
            }
        },
        "document": [
            {
                "name": "name",
                "url": ""
            },
            {
                "name": "name",
                "url": ""
            },
            {
                "name": "name",
                "url": ""
            }
        ]
    }
```

## Create a Supplier

**Description**

Create a supplier object.

**Parameters**

|name|type|description|
|---|---|---|
|id| long|Unique identifier for the object.|
|details| jsonb| Details for the object.|

**Return**

Returns the success status if the update succeeded. Returns an error if create parameters are invalid (e.g. specifying an invalid coupon or an invalid source).

**Curl Request**

    curl https://api.stripe.com/v1/customers \
    -u sk_test_4eC39HqLyjWDarjtT1zdp7dc: \
    -d description="My First Test Customer (created for API docs at https://www.stripe.com/docs/api)"

**Response**

```json   
{
    "code": 200,
    "message": "supplier added successfully",
    "type": "object",
    "object": []
}
```

## Update a Supplier

**Description**

Update a supplier object.

**Parameters**

|name|type|description|
|---|---|---|
|id| long|Unique identifier for the object.|
|details| jsonb| Details for the object.|

**Return**

Returns the success status if the update succeeded. Returns an error if create parameters are invalid (e.g. specifying an invalid coupon or an invalid source).

**Curl Request**

    curl https://api.stripe.com/v1/customers \
    -u sk_test_4eC39HqLyjWDarjtT1zdp7dc: \
    -d description="My First Test Customer (created for API docs at https://www.stripe.com/docs/api)"

**Response**

```json   
{
    "code": 200,
    "message": "supplier updated successfully",
    "type": "object",
    "object": []
}
```

## Delete a Supplier

**Description**

Delete a supplier object.

**Parameters**

|name|type|description|
|---|---|---|
|id| long|Unique identifier for the object.|
|details| jsonb| Details for the object.|

**Return**

Returns the success status if the update succeeded. Returns an error if create parameters are invalid (e.g. specifying an invalid coupon or an invalid source).

**Curl Request**

    curl https://api.stripe.com/v1/customers \
    -u sk_test_4eC39HqLyjWDarjtT1zdp7dc: \
    -d description="My First Test Customer (created for API docs at https://www.stripe.com/docs/api)"

**Response**

```json   
{
    "code": 200,
    "message": "supplier deleted successfully",
    "type": "object",
    "object": []
}
```

## Deactivate a Supplier

**Description**

Deactivate a supplier object.

**Parameters**

|name|type|description|
|---|---|---|
|id| long|Unique identifier for the object.|
|details| jsonb| Details for the object.|

**Return**

Returns the success status if the update succeeded. Returns an error if create parameters are invalid (e.g. specifying an invalid coupon or an invalid source).

**Curl Request**

    curl https://api.stripe.com/v1/customers \
    -u sk_test_4eC39HqLyjWDarjtT1zdp7dc: \
    -d description="My First Test Customer (created for API docs at https://www.stripe.com/docs/api)"

**Response**

```json   
{
    "code": 200,
    "message": "supplier deactivated successfully",
    "type": "object",
    "object": []
}
```

## Search Supplier

**Description**

Search a supplier object.

**Parameters**

|name|type|description|
|---|---|---|
|id| long|Unique identifier for the object.|
|details| jsonb| Details for the object.|

**Return**

Returns the success status if the update succeeded. Returns an error if create parameters are invalid (e.g. specifying an invalid coupon or an invalid source).

**Curl Request**

    curl https://api.stripe.com/v1/customers \
    -u sk_test_4eC39HqLyjWDarjtT1zdp7dc: \
    -d description="My First Test Customer (created for API docs at https://www.stripe.com/docs/api)"

**Response**

```json   
{
    "code": 200,
    "message": "supplier search successfully",
    "type": "object",
    "object": [*Array of resultant objects*]
}
```

# Currency

This object represents the Currency that is raised from the internal employees of the organization to any item.

**EndPoints**

    POST {{baseUrl}}/currency

    PUT {{baseUrl}}/currency
    
    DELETE {{baseUrl}}/currency/:id

    POST {{baseUrl}}/currency/deactivate/:id

    GET {{baseUrl}}/currency

## The Currency Object

**Attributes**

|name|type|description|
|---|---|---|
|id| long|Unique identifier for the object.|
|details| jsonb| Details for the object.|

**The Object**

```json 
  {
    "code": "INR",
    "name": "Rupee",
    "countryName": "INDIA",
    "countryCode": 91
}
```

## Create a Currency

**Description**

Create a currency object.

**Parameters**

|name|type|description|
|---|---|---|
|id| long|Unique identifier for the object.|
|details| jsonb| Details for the object.|

**Return**

Returns the success status if the update succeeded. Returns an error if create parameters are invalid (e.g. specifying an invalid coupon or an invalid source).

**Curl Request**

    curl https://api.stripe.com/v1/customers \
    -u sk_test_4eC39HqLyjWDarjtT1zdp7dc: \
    -d description="My First Test Customer (created for API docs at https://www.stripe.com/docs/api)"

**Response**

```json   
{
    "code": 200,
    "message": "currency added successfully",
    "type": "object",
    "object": []
}
```

## Update a Currency

**Description**

Update a currency object.

**Parameters**

|name|type|description|
|---|---|---|
|id| long|Unique identifier for the object.|
|details| jsonb| Details for the object.|

**Return**

Returns the success status if the update succeeded. Returns an error if create parameters are invalid (e.g. specifying an invalid coupon or an invalid source).

**Curl Request**

    curl https://api.stripe.com/v1/customers \
    -u sk_test_4eC39HqLyjWDarjtT1zdp7dc: \
    -d description="My First Test Customer (created for API docs at https://www.stripe.com/docs/api)"

**Response**

```json   
{
    "code": 200,
    "message": "currency updated successfully",
    "type": "object",
    "object": []
}
```

## Delete a Currency

**Description**

Delete a currency object.

**Parameters**

|name|type|description|
|---|---|---|
|id| long|Unique identifier for the object.|
|details| jsonb| Details for the object.|

**Return**

Returns the success status if the update succeeded. Returns an error if create parameters are invalid (e.g. specifying an invalid coupon or an invalid source).

**Curl Request**

    curl https://api.stripe.com/v1/customers \
    -u sk_test_4eC39HqLyjWDarjtT1zdp7dc: \
    -d description="My First Test Customer (created for API docs at https://www.stripe.com/docs/api)"

**Response**

```json   
{
    "code": 200,
    "message": "currency deleted successfully",
    "type": "object",
    "object": []
}
```

## Deactivate a Currency

**Description**

Deactivate a currency object.

**Parameters**

|name|type|description|
|---|---|---|
|id| long|Unique identifier for the object.|
|details| jsonb| Details for the object.|

**Return**

Returns the success status if the update succeeded. Returns an error if create parameters are invalid (e.g. specifying an invalid coupon or an invalid source).

**Curl Request**

    curl https://api.stripe.com/v1/customers \
    -u sk_test_4eC39HqLyjWDarjtT1zdp7dc: \
    -d description="My First Test Customer (created for API docs at https://www.stripe.com/docs/api)"

**Response**

```json   
{
    "code": 200,
    "message": "currency deactivated successfully",
    "type": "object",
    "object": []
}
```

## Search Currency

**Description**

Search a currency object.

**Parameters**

|name|type|description|
|---|---|---|
|id| long|Unique identifier for the object.|
|details| jsonb| Details for the object.|

**Return**

Returns the success status if the update succeeded. Returns an error if create parameters are invalid (e.g. specifying an invalid coupon or an invalid source).

**Curl Request**

    curl https://api.stripe.com/v1/customers \
    -u sk_test_4eC39HqLyjWDarjtT1zdp7dc: \
    -d description="My First Test Customer (created for API docs at https://www.stripe.com/docs/api)"

**Response**

```json   
{
    "code": 200,
    "message": "currency search successfully",
    "type": "object",
    "object": [*Array of resultant objects*]
}
```

# Location

This object represents the Location that is raised from the internal employees of the organization to any item.

**EndPoints**

    POST {{baseUrl}}/location

    PUT {{baseUrl}}/location/:id
    
    DELETE {{baseUrl}}/location/:id

    POST {{baseUrl}}/location/deactivate/:id

    GET {{baseUrl}}/location

## The Location Object

**Attributes**

|name|type|description|
|---|---|---|
|id| long|Unique identifier for the object.|
|details| jsonb| Details for the object.|

**The Object**

```json 
 {
    "name": "Rupee",
    "status":"ACTIVE"
}
```

## Create a Location

**Description**

Create a location object.

**Parameters**

|name|type|description|
|---|---|---|
|id| long|Unique identifier for the object.|
|details| jsonb| Details for the object.|

**Return**

Returns the success status if the update succeeded. Returns an error if create parameters are invalid (e.g. specifying an invalid coupon or an invalid source).

**Curl Request**

    curl https://api.stripe.com/v1/customers \
    -u sk_test_4eC39HqLyjWDarjtT1zdp7dc: \
    -d description="My First Test Customer (created for API docs at https://www.stripe.com/docs/api)"

**Response**

```json   
{
    "code": 200,
    "message": "location added successfully",
    "type": "object",
    "object": []
}
```

## Update a Location

**Description**

Update a location object.

**Parameters**

|name|type|description|
|---|---|---|
|id| long|Unique identifier for the object.|
|details| jsonb| Details for the object.|

**Return**

Returns the success status if the update succeeded. Returns an error if create parameters are invalid (e.g. specifying an invalid coupon or an invalid source).

**Curl Request**

    curl https://api.stripe.com/v1/customers \
    -u sk_test_4eC39HqLyjWDarjtT1zdp7dc: \
    -d description="My First Test Customer (created for API docs at https://www.stripe.com/docs/api)"

**Response**

```json   
{
    "code": 200,
    "message": "location updated successfully",
    "type": "object",
    "object": []
}
```

## Delete a Location

**Description**

Delete a location object.

**Parameters**

|name|type|description|
|---|---|---|
|id| long|Unique identifier for the object.|
|details| jsonb| Details for the object.|

**Return**

Returns the success status if the update succeeded. Returns an error if create parameters are invalid (e.g. specifying an invalid coupon or an invalid source).

**Curl Request**

    curl https://api.stripe.com/v1/customers \
    -u sk_test_4eC39HqLyjWDarjtT1zdp7dc: \
    -d description="My First Test Customer (created for API docs at https://www.stripe.com/docs/api)"

**Response**

```json   
{
    "code": 200,
    "message": "location deleted successfully",
    "type": "object",
    "object": []
}
```

## Deactivate a Location

**Description**

Deactivate a location object.

**Parameters**

|name|type|description|
|---|---|---|
|id| long|Unique identifier for the object.|
|details| jsonb| Details for the object.|

**Return**

Returns the success status if the update succeeded. Returns an error if create parameters are invalid (e.g. specifying an invalid coupon or an invalid source).

**Curl Request**

    curl https://api.stripe.com/v1/customers \
    -u sk_test_4eC39HqLyjWDarjtT1zdp7dc: \
    -d description="My First Test Customer (created for API docs at https://www.stripe.com/docs/api)"

**Response**

```json   
{
    "code": 200,
    "message": "location deactivated successfully",
    "type": "object",
    "object": []
}
```

## Search Location

**Description**

Search a location object.

**Parameters**

|name|type|description|
|---|---|---|
|id| long|Unique identifier for the object.|
|details| jsonb| Details for the object.|

**Return**

Returns the success status if the update succeeded. Returns an error if create parameters are invalid (e.g. specifying an invalid coupon or an invalid source).

**Curl Request**

    curl https://api.stripe.com/v1/customers \
    -u sk_test_4eC39HqLyjWDarjtT1zdp7dc: \
    -d description="My First Test Customer (created for API docs at https://www.stripe.com/docs/api)"

**Response**

```json   
{
    "code": 200,
    "message": "location search successfully",
    "type": "object",
    "object": [*Array of resultant objects*]
}
```

# Invoice

This object represents the Invoice that is raised from the internal employees of the organization to any item.

**EndPoints**

    POST {{baseUrl}}/invoice

    PUT {{baseUrl}}/invoice/:id
    
    DELETE {{baseUrl}}/invoice/:id

    POST {{baseUrl}}/invoice/deactivate/:id

    GET {{baseUrl}}/invoice

## The Invoice Object

**Attributes**

|name|type|description|
|---|---|---|
|id| long|Unique identifier for the object.|
|details| jsonb| Details for the object.|

**The Object**

```json 
{
        "url": "http://invoice-location.com",
        "issueDate": "15-01-2045",
        "invoiceDueDate": "15-01-2022",
        "amount": 24,
        "tax": "+18VAT",
        "purchaseOrder": {
            "id": 2,
            "requesterId": 1,
            "fromDate": "01-01-2022",
            "toDate": "02-01-2022",
            "createdOn": "03-01-2022",
            "updatedOn": "05-01-2022",
            "createdBy": "Creater Name",
            "updatedBy": "Updater Name",
            "deliveryDate": "10-01-2022",
            "status": "Pending | Unpaid | Undelivered | Delivered",
            "totalNumberOfProduct": "1",
            "totalAmount": 24,
            "paymentTerm": "30 Net",
            "shippingMethod": "Store Pickup",
            "paymentWith": "Credit card",
            "shippingTerms": "FOB",
            "notes": "this is notes for Purchase Order",
            "supplier": {
                "id": 2,
                "name": "raghav das",
                "email": "this@gmail.com",
                "contact": "+91 9876543210",
                "telephoneNo": "012-65432",
                "designationNo": "1233",
                "automateSending": "true",
                "city": "jaipur",
                "state": "rajasthan",
                "postalCode": "13468",
                "country": "USA",
                "paymentTerms": "terms",
                "category": "cat",
                "address": "Street no. B6, Miami",
                "status": "active",
                "company": {
                    "name": "flipkart",
                    "registrationNo": "123"
                },
                "bankDetails": {
                    "accountHolderName": "jitin",
                    "accountNo": "1234565789",
                    "bank": "ABCD",
                    "taxId": "DFS55465dFS",
                    "currency": {
                        "id": 1,
                        "code": "USD",
                        "name": "doller",
                        "countryName": "USA",
                        "countryCode": 1
                    }
                },
                "document": [
                    {
                        "name": "name",
                        "url": ""
                    },
                    {
                        "name": "name",
                        "url": ""
                    },
                    {
                        "name": "name",
                        "url": ""
                    }
                ]
            },
            "requestsDetail": [
                {
                    "requestId": 1,
                    "ids": [
                        1
                    ]
                }
            ],
            "purchaseOrderProduct": [
                {
                    "item": {
                        "id": 1,
                        "itemName": "mouse",
                        "itemType": "product",
                        "unit": "each",
                        "category": "tech",
                        "supplier": "flipkart",
                        "price": 12
                    },
                    "quantity": 2
                }
            ]
        },
        "currency": {
            "currencyId": 2,
            "code": "INR",
            "Name": "Rupee",
            "countryName": "INDIA",
            "countryCode": "91"
        }
    }
```

## Create a Invoice

**Description**

Create a invoice object.

**Parameters**

|name|type|description|
|---|---|---|
|id| long|Unique identifier for the object.|
|details| jsonb| Details for the object.|

**Return**

Returns the success status if the update succeeded. Returns an error if create parameters are invalid (e.g. specifying an invalid coupon or an invalid source).

**Curl Request**

    curl https://api.stripe.com/v1/customers \
    -u sk_test_4eC39HqLyjWDarjtT1zdp7dc: \
    -d description="My First Test Customer (created for API docs at https://www.stripe.com/docs/api)"

**Response**

```json   
{
    "code": 200,
    "message": "invoice added successfully",
    "type": "object",
    "object": []
}
```

## Update a Invoice

**Description**

Update a invoice object.

**Parameters**

|name|type|description|
|---|---|---|
|id| long|Unique identifier for the object.|
|details| jsonb| Details for the object.|

**Return**

Returns the success status if the update succeeded. Returns an error if create parameters are invalid (e.g. specifying an invalid coupon or an invalid source).

**Curl Request**

    curl https://api.stripe.com/v1/customers \
    -u sk_test_4eC39HqLyjWDarjtT1zdp7dc: \
    -d description="My First Test Customer (created for API docs at https://www.stripe.com/docs/api)"

**Response**

```json   
{
    "code": 200,
    "message": "invoice updated successfully",
    "type": "object",
    "object": []
}
```

## Delete a Invoice

**Description**

Delete a invoice object.

**Parameters**

|name|type|description|
|---|---|---|
|id| long|Unique identifier for the object.|
|details| jsonb| Details for the object.|

**Return**

Returns the success status if the update succeeded. Returns an error if create parameters are invalid (e.g. specifying an invalid coupon or an invalid source).

**Curl Request**

    curl https://api.stripe.com/v1/customers \
    -u sk_test_4eC39HqLyjWDarjtT1zdp7dc: \
    -d description="My First Test Customer (created for API docs at https://www.stripe.com/docs/api)"

**Response**

```json   
{
    "code": 200,
    "message": "invoice deleted successfully",
    "type": "object",
    "object": []
}
```

## Deactivate a Invoice

**Description**

Deactivate a invoice object.

**Parameters**

|name|type|description|
|---|---|---|
|id| long|Unique identifier for the object.|
|details| jsonb| Details for the object.|

**Return**

Returns the success status if the update succeeded. Returns an error if create parameters are invalid (e.g. specifying an invalid coupon or an invalid source).

**Curl Request**

    curl https://api.stripe.com/v1/customers \
    -u sk_test_4eC39HqLyjWDarjtT1zdp7dc: \
    -d description="My First Test Customer (created for API docs at https://www.stripe.com/docs/api)"

**Response**

```json   
{
    "code": 200,
    "message": "invoice deactivated successfully",
    "type": "object",
    "object": []
}
```

## Search Invoice

**Description**

Search a invoice object.

**Parameters**

|name|type|description|
|---|---|---|
|id| long|Unique identifier for the object.|
|details| jsonb| Details for the object.|

**Return**

Returns the success status if the update succeeded. Returns an error if create parameters are invalid (e.g. specifying an invalid coupon or an invalid source).

**Curl Request**

    curl https://api.stripe.com/v1/customers \
    -u sk_test_4eC39HqLyjWDarjtT1zdp7dc: \
    -d description="My First Test Customer (created for API docs at https://www.stripe.com/docs/api)"

**Response**

```json   
{
    "code": 200,
    "message": "invoice search successfully",
    "type": "object",
    "object": [*Array of resultant objects*]
}
```

# Purchase Order

This object represents the Purchase Order that is raised from the internal employees of the organization to any item.

**EndPoints**

    POST {{baseUrl}}/purchase_order

    PUT {{baseUrl}}/purchase_order/:id
    
    DELETE {{baseUrl}}/purchase_order/:id

    POST {{baseUrl}}/purchase_order/deactivate/:id

    GET {{baseUrl}}/purchase_order

## The Purchase Order Object

**Attributes**

|name|type|description|
|---|---|---|
|id| long|Unique identifier for the object.|
|details| jsonb| Details for the object.|

**The Object**

```json
{
        "requesterId": 1,
        "fromDate": "01-01-2022",
        "toDate": "02-01-2022",
        "createdOn": "03-01-2022",
        "updatedOn": "05-01-2022",
        "createdBy": "Creater Name",
        "updatedBy": "Updater Name",
        "deliveryDate": "10-01-2022",
        "status": "Pending | Unpaid | Undelivered | Delivered",
        "totalNumberOfProduct": "3",
        "totalAmount": 824,
        "paymentTerm": "30 Net",
        "shippingMethod": "Store Pickup",
        "paymentWith": "Credit card",
        "shippingTerms": "FOB",
        "notes": "notes sample",
        "supplier": {
            "id": 1,
            "name": "andrew choudhary",
            "email": "this@gmail.com",
            "contact": "+91 9876543210",
            "telephoneNo": "012-65432",
            "designationNo": "1233",
            "automateSending": "true",
            "city": "jaipur",
            "state": "rajasthan",
            "postalCode": "13468",
            "country": "USA",
            "paymentTerms": "terms",
            "category": "cat",
            "address": "Street no. B6, Miami",
            "status": "active",
            "company": {
                "name": "amazone",
                "registrationNo": "123"
            },
            "bankDetails": {
                "accountHolderName": "jitin",
                "accountNo": "1234565789",
                "bank": "ABCD",
                "taxId": "DFS55465dFS",
                "currency": {
                    "id": 1,
                    "code": "USD",
                    "name": "doller",
                    "countryName": "USA",
                    "countryCode": 1
                }
            },
            "document": [
                {
                    "name": "name",
                    "url": ""
                },
                {
                    "name": "name",
                    "url": ""
                },
                {
                    "name": "name",
                    "url": ""
                }
            ]
        },
        "requestsDetail": [
            {
                "requestId": 1,
                "ids": [
                    2
                ]
            },
            {
                "requestId": 2,
                "ids": [
                    1
                ]
            }
        ],
        "purchaseOrderProducts": [
            {
                "item": {
                    "id": 2,
                    "itemName": "hp laptop",
                    "itemType": "product",
                    "unit": "each",
                    "supplier": "amazone",
                    "category": "tech",
                    "price": 800
                },
                "quantity": 1
            },
            {
                "item": {
                    "id": 1,
                    "itemName": "mouse",
                    "itemType": "product",
                    "unit": "each",
                    "category": "tech",
                    "supplier": "amazone",
                    "price": 12
                },
                "quantity": 2
            }
        ]
    } 
```

## Create a Purchase Order

**Description**

Create a purchase order object.

**Parameters**

|name|type|description|
|---|---|---|
|id| long|Unique identifier for the object.|
|details| jsonb| Details for the object.|

**Return**

Returns the success status if the update succeeded. Returns an error if create parameters are invalid (e.g. specifying an invalid coupon or an invalid source).

**Curl Request**

    curl https://api.stripe.com/v1/customers \
    -u sk_test_4eC39HqLyjWDarjtT1zdp7dc: \
    -d description="My First Test Customer (created for API docs at https://www.stripe.com/docs/api)"

**Response**

```json   
{
    "code": 200,
    "message": "purchase order added successfully",
    "type": "object",
    "object": []
}
```

## Update a Purchase Order

**Description**

Update a purchase order object.

**Parameters**

|name|type|description|
|---|---|---|
|id| long|Unique identifier for the object.|
|details| jsonb| Details for the object.|

**Return**

Returns the success status if the update succeeded. Returns an error if create parameters are invalid (e.g. specifying an invalid coupon or an invalid source).

**Curl Request**

    curl https://api.stripe.com/v1/customers \
    -u sk_test_4eC39HqLyjWDarjtT1zdp7dc: \
    -d description="My First Test Customer (created for API docs at https://www.stripe.com/docs/api)"

**Response**

```json   
{
    "code": 200,
    "message": "purchase order updated successfully",
    "type": "object",
    "object": []
}
```

## Delete a Purchase Order

**Description**

Delete a purchase order object.

**Parameters**

|name|type|description|
|---|---|---|
|id| long|Unique identifier for the object.|
|details| jsonb| Details for the object.|

**Return**

Returns the success status if the update succeeded. Returns an error if create parameters are invalid (e.g. specifying an invalid coupon or an invalid source).

**Curl Request**

    curl https://api.stripe.com/v1/customers \
    -u sk_test_4eC39HqLyjWDarjtT1zdp7dc: \
    -d description="My First Test Customer (created for API docs at https://www.stripe.com/docs/api)"

**Response**

```json   
{
    "code": 200,
    "message": "purchase order deleted successfully",
    "type": "object",
    "object": []
}
```

## Deactivate a Purchase Order

**Description**

Deactivate a purchase order object.

**Parameters**

|name|type|description|
|---|---|---|
|id| long|Unique identifier for the object.|
|details| jsonb| Details for the object.|

**Return**

Returns the success status if the update succeeded. Returns an error if create parameters are invalid (e.g. specifying an invalid coupon or an invalid source).

**Curl Request**

    curl https://api.stripe.com/v1/customers \
    -u sk_test_4eC39HqLyjWDarjtT1zdp7dc: \
    -d description="My First Test Customer (created for API docs at https://www.stripe.com/docs/api)"

**Response**

```json   
{
    "code": 200,
    "message": "purchase order deactivated successfully",
    "type": "object",
    "object": []
}
```

## Search Purchase Order

**Description**

Search a purchase order object.

**Parameters**

|name|type|description|
|---|---|---|
|id| long|Unique identifier for the object.|
|details| jsonb| Details for the object.|

**Return**

Returns the success status if the update succeeded. Returns an error if create parameters are invalid (e.g. specifying an invalid coupon or an invalid source).

**Curl Request**

    curl https://api.stripe.com/v1/customers \
    -u sk_test_4eC39HqLyjWDarjtT1zdp7dc: \
    -d description="My First Test Customer (created for API docs at https://www.stripe.com/docs/api)"

**Response**

```json   
{
    "code": 200,
    "message": "purchase order search successfully",
    "type": "object",
    "object": [*Array of resultant objects*]
}
```

# Quotation

This object represents the Quotation that is raised from the internal employees of the organization to any item.

**EndPoints**

    POST {{baseUrl}}/quotation

    PUT {{baseUrl}}/quotation/:id
    
    DELETE {{baseUrl}}/quotation

    POST {{baseUrl}}/quotation/deactivate/:id

    GET https://u4kzlb58qh.execute-api.us-east-1.amazonaws.com/procurement-dev/quotation?id=71

## The Quotation Object

**Attributes**

|name|type|description|
|---|---|---|
|id| long|Unique identifier for the object.|
|details| jsonb| Details for the object.|

**The Object**

```json
 {
    "openDate": "01-01-2000",
    "closingDate": "01-01-2000",
    "requiredDeliveryDate": "01-01-2000",
    "rfqType": "this",
    "location": "head office",
    "note": "this is note",
    "products": [
        {
            "item": {
                "id": 1,
                "details": {
                    "itemName": "mouse",
                    "price": 12,
                    "unit": "each",
                    "itemType": "product",
                    "category": "tech",
                    "supplier": {
                        "id": 1,
                        "name": "andrew choudhary",
                        "email": "this@gmail.com",
                        "contact": "+91 9876543210",
                        "telephoneNo": "012-65432",
                        "designationNo": "1233",
                        "automateSending": "true",
                        "city": "jaipur",
                        "state": "rajasthan",
                        "postalCode": "13468",
                        "country": "USA",
                        "paymentTerms": "terms",
                        "category": "cat",
                        "address": "Street no. B6, Miami",
                        "status": "active",
                        "company": {
                            "name": "amazone",
                            "registrationNo": "123"
                        },
                        "bankDetails": {
                            "accountHolderName": "jitin",
                            "accountNo": "1234565789",
                            "bank": "ABCD",
                            "taxId": "DFS55465dFS",
                            "currency": {
                                "id": 1,
                                "code": "USD",
                                "name": "doller",
                                "countryName": "USA",
                                "countryCode": 1
                            }
                        },
                        "document": [
                            {
                                "name": "name",
                                "url": ""
                            },
                            {
                                "name": "name",
                                "url": ""
                            },
                            {
                                "name": "name",
                                "url": ""
                            }
                        ]
                    }
                }
            },
            "quantity": 2
        },
        {
            "item": {
                "id": 1,
                "itemName": "mouse",
                "price": 12,
                "unit": "each",
                "itemType": "product",
                "category": "tech",
                "supplier": {
                    "id": 1,
                    "name": "andrew choudhary",
                    "email": "this@gmail.com",
                    "contact": "+91 9876543210",
                    "telephoneNo": "012-65432",
                    "designationNo": "1233",
                    "automateSending": "true",
                    "city": "jaipur",
                    "state": "rajasthan",
                    "postalCode": "13468",
                    "country": "USA",
                    "paymentTerms": "terms",
                    "category": "cat",
                    "address": "Street no. B6, Miami",
                    "status": "active",
                    "company": {
                        "name": "amazone",
                        "registrationNo": "123"
                    },
                    "bankDetails": {
                        "accountHolderName": "jitin",
                        "accountNo": "1234565789",
                        "bank": "ABCD",
                        "taxId": "DFS55465dFS",
                        "currency": {
                            "id": 1,
                            "code": "USD",
                            "name": "doller",
                            "countryName": "USA",
                            "countryCode": 1
                        }
                    },
                    "document": [
                        {
                            "name": "name",
                            "url": ""
                        },
                        {
                            "name": "name",
                            "url": ""
                        },
                        {
                            "name": "name",
                            "url": ""
                        }
                    ]
                }
            },
            "quantity": 2
        }
    ],
    "paymentTerms": "terms",
    "paymentMode": "ABCD",
    "incoterms": "ABCD",
    "modeOfDelivery": "accountHolderName",
    "document": [
        {
            "name": "name",
            "url": ""
        },
        {
            "name": "name",
            "url": ""
        },
        {
            "name": "name",
            "url": ""
        }
    ]
}
```

## Create a Quotation

**Description**

Create a quotation object.

**Parameters**

|name|type|description|
|---|---|---|
|id| long|Unique identifier for the object.|
|details| jsonb| Details for the object.|

**Return**

Returns the success status if the update succeeded. Returns an error if create parameters are invalid (e.g. specifying an invalid coupon or an invalid source).

**Curl Request**

    curl https://api.stripe.com/v1/customers \
    -u sk_test_4eC39HqLyjWDarjtT1zdp7dc: \
    -d description="My First Test Customer (created for API docs at https://www.stripe.com/docs/api)"

**Response**

```json   
{
    "code": 200,
    "message": "quotation added successfully",
    "type": "object",
    "object": []
}
```

## Update a Quotation

**Description**

Update a quotation object.

**Parameters**

|name|type|description|
|---|---|---|
|id| long|Unique identifier for the object.|
|details| jsonb| Details for the object.|

**Return**

Returns the success status if the update succeeded. Returns an error if create parameters are invalid (e.g. specifying an invalid coupon or an invalid source).

**Curl Request**

    curl https://api.stripe.com/v1/customers \
    -u sk_test_4eC39HqLyjWDarjtT1zdp7dc: \
    -d description="My First Test Customer (created for API docs at https://www.stripe.com/docs/api)"

**Response**

```json   
{
    "code": 200,
    "message": "quotation updated successfully",
    "type": "object",
    "object": []
}
```

## Delete a Quotation

**Description**

Delete a quotation object.

**Parameters**

|name|type|description|
|---|---|---|
|id| long|Unique identifier for the object.|
|details| jsonb| Details for the object.|

**Return**

Returns the success status if the update succeeded. Returns an error if create parameters are invalid (e.g. specifying an invalid coupon or an invalid source).

**Curl Request**

    curl https://api.stripe.com/v1/customers \
    -u sk_test_4eC39HqLyjWDarjtT1zdp7dc: \
    -d description="My First Test Customer (created for API docs at https://www.stripe.com/docs/api)"

**Response**

```json   
{
    "code": 200,
    "message": "quotation deleted successfully",
    "type": "object",
    "object": []
}
```

## Deactivate a Quotation

**Description**

Deactivate a quotation object.

**Parameters**

|name|type|description|
|---|---|---|
|id| long|Unique identifier for the object.|
|details| jsonb| Details for the object.|

**Return**

Returns the success status if the update succeeded. Returns an error if create parameters are invalid (e.g. specifying an invalid coupon or an invalid source).

**Curl Request**

    curl https://api.stripe.com/v1/customers \
    -u sk_test_4eC39HqLyjWDarjtT1zdp7dc: \
    -d description="My First Test Customer (created for API docs at https://www.stripe.com/docs/api)"

**Response**

```json   
{
    "code": 200,
    "message": "quotation deactivated successfully",
    "type": "object",
    "object": []
}
```

## Search Quotation

**Description**

Search a quotation object.

**Parameters**

|name|type|description|
|---|---|---|
|id| long|Unique identifier for the object.|
|details| jsonb| Details for the object.|

**Return**

Returns the success status if the update succeeded. Returns an error if create parameters are invalid (e.g. specifying an invalid coupon or an invalid source).

**Curl Request**

    curl https://api.stripe.com/v1/customers \
    -u sk_test_4eC39HqLyjWDarjtT1zdp7dc: \
    -d description="My First Test Customer (created for API docs at https://www.stripe.com/docs/api)"

**Response**

```json   
{
    "code": 200,
    "message": "quotation search successfully",
    "type": "object",
    "object": [*Array of resultant objects*]
}
```

# Approvers

This object represents the Approvers that is raised from the internal employees of the organization to any item.

**EndPoints**

    POST {{baseUrl}}/approvers

    PUT {{baseUrl}}/approvers/:id
    
    DELETE {{baseUrl}}/approvers/:id

    GET {{baseUrl}}/approvers

## The Approvers Object

**Attributes**

|name|type|description|
|---|---|---|
|id| long|Unique identifier for the object.|
|details| jsonb| Details for the object.|

**The Object**

```json
 {
    "allApprovers": [
        {
            "userId": "Axiu2818",
            "minAmount": "100",
            "maxAmount": "500",
            "location": "N. virginia",
            "order": "0"
        },
        {
            "userId": "uxiu281fdf8",
            "minAmount": "100",
            "maxAmount": "500",
            "location": "N. virginia",
            "order": "1"
        },
        {
            "userId": "bhiu2818",
            "minAmount": "100",
            "maxAmount": "500",
            "location": "N. virginia",
            "order": "2"
        }
    ]
}
```

## Create a Approvers

**Description**

Create a approvers object.

**Parameters**

|name|type|description|
|---|---|---|
|id| long|Unique identifier for the object.|
|details| jsonb| Details for the object.|

**Return**

Returns the success status if the update succeeded. Returns an error if create parameters are invalid (e.g. specifying an invalid coupon or an invalid source).

**Curl Request**

    curl https://api.stripe.com/v1/customers \
    -u sk_test_4eC39HqLyjWDarjtT1zdp7dc: \
    -d description="My First Test Customer (created for API docs at https://www.stripe.com/docs/api)"

**Response**

```json   
{
    "code": 200,
    "message": "approvers added successfully",
    "type": "object",
    "object": []
}
```

## Update a Approvers

**Description**

Update a approvers object.

**Parameters**

|name|type|description|
|---|---|---|
|id| long|Unique identifier for the object.|
|details| jsonb| Details for the object.|

**Return**

Returns the success status if the update succeeded. Returns an error if create parameters are invalid (e.g. specifying an invalid coupon or an invalid source).

**Curl Request**

    curl https://api.stripe.com/v1/customers \
    -u sk_test_4eC39HqLyjWDarjtT1zdp7dc: \
    -d description="My First Test Customer (created for API docs at https://www.stripe.com/docs/api)"

**Response**

```json   
{
    "code": 200,
    "message": "approvers updated successfully",
    "type": "object",
    "object": []
}
```

## Delete a Approvers

**Description**

Delete a approvers object.

**Parameters**

|name|type|description|
|---|---|---|
|id| long|Unique identifier for the object.|
|details| jsonb| Details for the object.|

**Return**

Returns the success status if the update succeeded. Returns an error if create parameters are invalid (e.g. specifying an invalid coupon or an invalid source).

**Curl Request**

    curl https://api.stripe.com/v1/customers \
    -u sk_test_4eC39HqLyjWDarjtT1zdp7dc: \
    -d description="My First Test Customer (created for API docs at https://www.stripe.com/docs/api)"

**Response**

```json   
{
    "code": 200,
    "message": "approvers deleted successfully",
    "type": "object",
    "object": []
}
```

## Search Approvers

**Description**

Search a approvers object.

**Parameters**

|name|type|description|
|---|---|---|
|id| long|Unique identifier for the object.|
|details| jsonb| Details for the object.|

**Return**

Returns the success status if the update succeeded. Returns an error if create parameters are invalid (e.g. specifying an invalid coupon or an invalid source).

**Curl Request**

    curl https://api.stripe.com/v1/customers \
    -u sk_test_4eC39HqLyjWDarjtT1zdp7dc: \
    -d description="My First Test Customer (created for API docs at https://www.stripe.com/docs/api)"

**Response**

```json   
{
    "code": 200,
    "message": "approvers search successfully",
    "type": "object",
    "object": [*Array of resultant objects*]
}
```

# Company Profile

This object represents the Company Profile that is raised from the internal employees of the organization to any item.

**EndPoints**

    POST {{baseUrl}}/company_profile

    PUT {{baseUrl}}/company_profile/:id
    
    DELETE {{baseUrl}}/company_profile/:id

    GET {{baseUrl}}/company_profile

## The Company Profile Object

**Attributes**

|name|type|description|
|---|---|---|
|id| long|Unique identifier for the object.|
|details| jsonb| Details for the object.|

**The Object**

```json
 {
    "accountHolderName": "This is name",
    "companyName": "company",
    "country": "country",
    "state": "state",
    "emailAddress": "email@email.com",
    "contactNo": "987654321",
    "date": "01-01-1000",
    "address": "address"
}
```

## Create a Company Profile

**Description**

Create a company profile object.

**Parameters**

|name|type|description|
|---|---|---|
|id| long|Unique identifier for the object.|
|details| jsonb| Details for the object.|

**Return**

Returns the success status if the update succeeded. Returns an error if create parameters are invalid (e.g. specifying an invalid coupon or an invalid source).

**Curl Request**

    curl https://api.stripe.com/v1/customers \
    -u sk_test_4eC39HqLyjWDarjtT1zdp7dc: \
    -d description="My First Test Customer (created for API docs at https://www.stripe.com/docs/api)"

**Response**

```json   
{
    "code": 200,
    "message": "company profile added successfully",
    "type": "object",
    "object": []
}
```

## Update a Company Profile

**Description**

Update a company profile object.

**Parameters**

|name|type|description|
|---|---|---|
|id| long|Unique identifier for the object.|
|details| jsonb| Details for the object.|

**Return**

Returns the success status if the update succeeded. Returns an error if create parameters are invalid (e.g. specifying an invalid coupon or an invalid source).

**Curl Request**

    curl https://api.stripe.com/v1/customers \
    -u sk_test_4eC39HqLyjWDarjtT1zdp7dc: \
    -d description="My First Test Customer (created for API docs at https://www.stripe.com/docs/api)"

**Response**

```json   
{
    "code": 200,
    "message": "company profile updated successfully",
    "type": "object",
    "object": []
}
```

## Delete a Company Profile

**Description**

Delete a company profile object.

**Parameters**

|name|type|description|
|---|---|---|
|id| long|Unique identifier for the object.|
|details| jsonb| Details for the object.|

**Return**

Returns the success status if the update succeeded. Returns an error if create parameters are invalid (e.g. specifying an invalid coupon or an invalid source).

**Curl Request**

    curl https://api.stripe.com/v1/customers \
    -u sk_test_4eC39HqLyjWDarjtT1zdp7dc: \
    -d description="My First Test Customer (created for API docs at https://www.stripe.com/docs/api)"

**Response**

```json   
{
    "code": 200,
    "message": "company profile deleted successfully",
    "type": "object",
    "object": []
}
```

## Search Company Profile

**Description**

Search a company profile object.

**Parameters**

|name|type|description|
|---|---|---|
|id| long|Unique identifier for the object.|
|details| jsonb| Details for the object.|

**Return**

Returns the success status if the update succeeded. Returns an error if create parameters are invalid (e.g. specifying an invalid coupon or an invalid source).

**Curl Request**

    curl https://api.stripe.com/v1/customers \
    -u sk_test_4eC39HqLyjWDarjtT1zdp7dc: \
    -d description="My First Test Customer (created for API docs at https://www.stripe.com/docs/api)"

**Response**

```json   
{
    "code": 200,
    "message": "company profile search successfully",
    "type": "object",
    "object": [*Array of resultant objects*]
}
```

# Send Email

This object represents the Send Email that is raised from the internal employees of the organization to any item.

**EndPoints**

    POST {{baseUrl}}/email

    GET {{baseUrl}}/email?from=jkgoyal85@gmail.com

## The Send Email Object

**Attributes**

|name|type|description|
|---|---|---|
|id| long|Unique identifier for the object.|
|details| jsonb| Details for the object.|

**The Object**

```json
 {
    "from": "jkgoyal85@gmail.com",
    "to": [
        "jkg3358191@gmail.com"
    ],
    "content": "This is testing from lambda with variables",
    "subject": "subject1111",
    "attachment": "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcROR0O2H-FusQQa0AetWhBuspFurVB7p4DAkiq9sZ8&s"
}
```

## Create Send Email

**Description**

Create a send email object.

**Parameters**

|name|type|description|
|---|---|---|
|id| long|Unique identifier for the object.|
|details| jsonb| Details for the object.|

**Return**

Returns the success status if the update succeeded. Returns an error if create parameters are invalid (e.g. specifying an invalid coupon or an invalid source).

**Curl Request**

    curl https://api.stripe.com/v1/customers \
    -u sk_test_4eC39HqLyjWDarjtT1zdp7dc: \
    -d description="My First Test Customer (created for API docs at https://www.stripe.com/docs/api)"

**Response**

```json   
{
    "code": 200,
    "message": "send email added successfully",
    "type": "object",
    "object": []
}
```

## Search Send Email

**Description**

Search a send email object.

**Parameters**

|name|type|description|
|---|---|---|
|id| long|Unique identifier for the object.|
|details| jsonb| Details for the object.|

**Return**

Returns the success status if the update succeeded. Returns an error if create parameters are invalid (e.g. specifying an invalid coupon or an invalid source).

**Curl Request**

    curl https://api.stripe.com/v1/customers \
    -u sk_test_4eC39HqLyjWDarjtT1zdp7dc: \
    -d description="My First Test Customer (created for API docs at https://www.stripe.com/docs/api)"

**Response**

```json   
{
    "code": 200,
    "message": "send email search successfully",
    "type": "object",
    "object": [*Array of resultant objects*]
}
```

# Contact

This object represents the Contact that is raised from the internal employees of the organization to any item.

**EndPoints**

    POST {{baseUrl}}/contact

    PUT {{baseUrl}}/contact/:id
    
    DELETE {{baseUrl}}/contact/:id

    POST {{baseUrl}}/department/deactivate/:id

    GET {{baseUrl}}/contact

## The Contact Object

**Attributes**

|name|type|description|
|---|---|---|
|id| long|Unique identifier for the object.|
|details| jsonb| Details for the object.|

**The Object**

```json
 {
    "company": "Klein, Dach and Zulauf",
    "email": "Noah78@hotmail.com",
    "name": "Doyle Hand",
    "position": "Ergonomic reciprocal definition",
    "profile": "http://placeimg.com/640/480",
    "contNo": 1580330181,
    "status": "ACTIVE"
}
```

## Create a Contact

**Description**

Create a contact object.

**Parameters**

|name|type|description|
|---|---|---|
|id| long|Unique identifier for the object.|
|details| jsonb| Details for the object.|

**Return**

Returns the success status if the update succeeded. Returns an error if create parameters are invalid (e.g. specifying an invalid coupon or an invalid source).

**Curl Request**

    curl https://api.stripe.com/v1/customers \
    -u sk_test_4eC39HqLyjWDarjtT1zdp7dc: \
    -d description="My First Test Customer (created for API docs at https://www.stripe.com/docs/api)"

**Response**

```json   
{
    "code": 200,
    "message": "contact added successfully",
    "type": "object",
    "object": []
}
```

## Update a Contact

**Description**

Update a contact object.

**Parameters**

|name|type|description|
|---|---|---|
|id| long|Unique identifier for the object.|
|details| jsonb| Details for the object.|

**Return**

Returns the success status if the update succeeded. Returns an error if create parameters are invalid (e.g. specifying an invalid coupon or an invalid source).

**Curl Request**

    curl https://api.stripe.com/v1/customers \
    -u sk_test_4eC39HqLyjWDarjtT1zdp7dc: \
    -d description="My First Test Customer (created for API docs at https://www.stripe.com/docs/api)"

**Response**

```json   
{
    "code": 200,
    "message": "contact updated successfully",
    "type": "object",
    "object": []
}
```

## Delete a Contact

**Description**

Delete a contact object.

**Parameters**

|name|type|description|
|---|---|---|
|id| long|Unique identifier for the object.|
|details| jsonb| Details for the object.|

**Return**

Returns the success status if the update succeeded. Returns an error if create parameters are invalid (e.g. specifying an invalid coupon or an invalid source).

**Curl Request**

    curl https://api.stripe.com/v1/customers \
    -u sk_test_4eC39HqLyjWDarjtT1zdp7dc: \
    -d description="My First Test Customer (created for API docs at https://www.stripe.com/docs/api)"

**Response**

```json   
{
    "code": 200,
    "message": "contact deleted successfully",
    "type": "object",
    "object": []
}
```

## Deactivate a Contact

**Description**

Deactivate a contact object.

**Parameters**

|name|type|description|
|---|---|---|
|id| long|Unique identifier for the object.|
|details| jsonb| Details for the object.|

**Return**

Returns the success status if the update succeeded. Returns an error if create parameters are invalid (e.g. specifying an invalid coupon or an invalid source).

**Curl Request**

    curl https://api.stripe.com/v1/customers \
    -u sk_test_4eC39HqLyjWDarjtT1zdp7dc: \
    -d description="My First Test Customer (created for API docs at https://www.stripe.com/docs/api)"

**Response**

```json   
{
    "code": 200,
    "message": "contact deactivated successfully",
    "type": "object",
    "object": []
}
```

## Search Contact

**Description**

Search a contact object.

**Parameters**

|name|type|description|
|---|---|---|
|id| long|Unique identifier for the object.|
|details| jsonb| Details for the object.|

**Return**

Returns the success status if the update succeeded. Returns an error if create parameters are invalid (e.g. specifying an invalid coupon or an invalid source).

**Curl Request**

    curl https://api.stripe.com/v1/customers \
    -u sk_test_4eC39HqLyjWDarjtT1zdp7dc: \
    -d description="My First Test Customer (created for API docs at https://www.stripe.com/docs/api)"

**Response**

```json   
{
    "code": 200,
    "message": "contact search successfully",
    "type": "object",
    "object": [*Array of resultant objects*]
}
```

# Notification

This object represents the Notification that is raised from the internal employees of the organization to any item.

**EndPoints**

    POST {{baseUrl}}/notification

    PUT {{baseUrl}}/notification/:id
    
    DELETE {{baseUrl}}/notification/:id

    POST {{baseUrl}}/notification/deactivate/id

    GET {{baseUrl}}/notification

## The Notification Object

**Attributes**

|name|type|description|
|---|---|---|
|id| long|Unique identifier for the object.|
|details| jsonb| Details for the object.|

**The Object**

```json
 {
        "title": "Milan.Braun20",
        "img": "http://placeimg.com/640/480",
        "description": "sequi",
        "status": "ACTIVE"
}
```

## Create a Notification

**Description**

Create a notification object.

**Parameters**

|name|type|description|
|---|---|---|
|id| long|Unique identifier for the object.|
|details| jsonb| Details for the object.|

**Return**

Returns the success status if the update succeeded. Returns an error if create parameters are invalid (e.g. specifying an invalid coupon or an invalid source).

**Curl Request**

    curl https://api.stripe.com/v1/customers \
    -u sk_test_4eC39HqLyjWDarjtT1zdp7dc: \
    -d description="My First Test Customer (created for API docs at https://www.stripe.com/docs/api)"

**Response**

```json   
{
    "code": 200,
    "message": "notification added successfully",
    "type": "object",
    "object": []
}
```

## Update a Notification

**Description**

Update a notification object.

**Parameters**

|name|type|description|
|---|---|---|
|id| long|Unique identifier for the object.|
|details| jsonb| Details for the object.|

**Return**

Returns the success status if the update succeeded. Returns an error if create parameters are invalid (e.g. specifying an invalid coupon or an invalid source).

**Curl Request**

    curl https://api.stripe.com/v1/customers \
    -u sk_test_4eC39HqLyjWDarjtT1zdp7dc: \
    -d description="My First Test Customer (created for API docs at https://www.stripe.com/docs/api)"

**Response**

```json   
{
    "code": 200,
    "message": "notification updated successfully",
    "type": "object",
    "object": []
}
```

## Delete a Notification

**Description**

Delete a notification object.

**Parameters**

|name|type|description|
|---|---|---|
|id| long|Unique identifier for the object.|
|details| jsonb| Details for the object.|

**Return**

Returns the success status if the update succeeded. Returns an error if create parameters are invalid (e.g. specifying an invalid coupon or an invalid source).

**Curl Request**

    curl https://api.stripe.com/v1/customers \
    -u sk_test_4eC39HqLyjWDarjtT1zdp7dc: \
    -d description="My First Test Customer (created for API docs at https://www.stripe.com/docs/api)"

**Response**

```json   
{
    "code": 200,
    "message": "notification deleted successfully",
    "type": "object",
    "object": []
}
```

## Deactivate a Notification

**Description**

Deactivate a notification object.

**Parameters**

|name|type|description|
|---|---|---|
|id| long|Unique identifier for the object.|
|details| jsonb| Details for the object.|

**Return**

Returns the success status if the update succeeded. Returns an error if create parameters are invalid (e.g. specifying an invalid coupon or an invalid source).

**Curl Request**

    curl https://api.stripe.com/v1/customers \
    -u sk_test_4eC39HqLyjWDarjtT1zdp7dc: \
    -d description="My First Test Customer (created for API docs at https://www.stripe.com/docs/api)"

**Response**

```json   
{
    "code": 200,
    "message": "notification deactivated successfully",
    "type": "object",
    "object": []
}
```

## Search Notification

**Description**

Search a notification object.

**Parameters**

|name|type|description|
|---|---|---|
|id| long|Unique identifier for the object.|
|details| jsonb| Details for the object.|

**Return**

Returns the success status if the update succeeded. Returns an error if create parameters are invalid (e.g. specifying an invalid coupon or an invalid source).

**Curl Request**

    curl https://api.stripe.com/v1/customers \
    -u sk_test_4eC39HqLyjWDarjtT1zdp7dc: \
    -d description="My First Test Customer (created for API docs at https://www.stripe.com/docs/api)"

**Response**

```json   
{
    "code": 200,
    "message": "notification search successfully",
    "type": "object",
    "object": [*Array of resultant objects*]
}
```

# Department

This object represents the Department that is raised from the internal employees of the organization to any item.

**EndPoints**

    POST {{baseUrl}}/department

    PUT {{baseUrl}}/department/:id
    
    DELETE {{baseUrl}}/department/id

    POST {{baseUrl}}/department/deactivate/:id

    GET {{baseUrl}}/department

## The Department Object

**Attributes**

|name|type|description|
|---|---|---|
|id| long|Unique identifier for the object.|
|details| jsonb| Details for the object.|

**The Object**

```json
 {
    "name": "toys",
    "status": "ACTIVE"
}
```

## Create a Department

**Description**

Create a department object.

**Parameters**

|name|type|description|
|---|---|---|
|id| long|Unique identifier for the object.|
|details| jsonb| Details for the object.|

**Return**

Returns the success status if the update succeeded. Returns an error if create parameters are invalid (e.g. specifying an invalid coupon or an invalid source).

**Curl Request**

    curl https://api.stripe.com/v1/customers \
    -u sk_test_4eC39HqLyjWDarjtT1zdp7dc: \
    -d description="My First Test Customer (created for API docs at https://www.stripe.com/docs/api)"

**Response**

```json   
{
    "code": 200,
    "message": "department added successfully",
    "type": "object",
    "object": []
}
```

## Update a Department

**Description**

Update a department object.

**Parameters**

|name|type|description|
|---|---|---|
|id| long|Unique identifier for the object.|
|details| jsonb| Details for the object.|

**Return**

Returns the success status if the update succeeded. Returns an error if create parameters are invalid (e.g. specifying an invalid coupon or an invalid source).

**Curl Request**

    curl https://api.stripe.com/v1/customers \
    -u sk_test_4eC39HqLyjWDarjtT1zdp7dc: \
    -d description="My First Test Customer (created for API docs at https://www.stripe.com/docs/api)"

**Response**

```json   
{
    "code": 200,
    "message": "department updated successfully",
    "type": "object",
    "object": []
}
```

## Delete a Department

**Description**

Delete a department object.

**Parameters**

|name|type|description|
|---|---|---|
|id| long|Unique identifier for the object.|
|details| jsonb| Details for the object.|

**Return**

Returns the success status if the update succeeded. Returns an error if create parameters are invalid (e.g. specifying an invalid coupon or an invalid source).

**Curl Request**

    curl https://api.stripe.com/v1/customers \
    -u sk_test_4eC39HqLyjWDarjtT1zdp7dc: \
    -d description="My First Test Customer (created for API docs at https://www.stripe.com/docs/api)"

**Response**

```json   
{
    "code": 200,
    "message": "department deleted successfully",
    "type": "object",
    "object": []
}
```

## Deactivate a Department

**Description**

Deactivate a department object.

**Parameters**

|name|type|description|
|---|---|---|
|id| long|Unique identifier for the object.|
|details| jsonb| Details for the object.|

**Return**

Returns the success status if the update succeeded. Returns an error if create parameters are invalid (e.g. specifying an invalid coupon or an invalid source).

**Curl Request**

    curl https://api.stripe.com/v1/customers \
    -u sk_test_4eC39HqLyjWDarjtT1zdp7dc: \
    -d description="My First Test Customer (created for API docs at https://www.stripe.com/docs/api)"

**Response**

```json   
{
    "code": 200,
    "message": "department deactivated successfully",
    "type": "object",
    "object": []
}
```

## Search Department

**Description**

Search a department object.

**Parameters**

|name|type|description|
|---|---|---|
|id| long|Unique identifier for the object.|
|details| jsonb| Details for the object.|

**Return**

Returns the success status if the update succeeded. Returns an error if create parameters are invalid (e.g. specifying an invalid coupon or an invalid source).

**Curl Request**

    curl https://api.stripe.com/v1/customers \
    -u sk_test_4eC39HqLyjWDarjtT1zdp7dc: \
    -d description="My First Test Customer (created for API docs at https://www.stripe.com/docs/api)"

**Response**

```json   
{
    "code": 200,
    "message": "department search successfully",
    "type": "object",
    "object": [*Array of resultant objects*]
}
```

# Kanban

This object represents the Kanban that is raised from the internal employees of the organization to any item.

**EndPoints**

    POST {{baseUrl}}/kanban

    PUT {{baseUrl}}/kanban/:id
    
    DELETE {{baseUrl}}/kanban/:id

    POST {{baseUrl}}/kanban/deactivate/2:id

    GET {{baseUrl}}/kanban

## The Kanban Object

**Attributes**

|name|type|description|
|---|---|---|
|id| long|Unique identifier for the object.|
|details| jsonb| Details for the object.|

**The Object**

```json
 {
    "title": "sint architecto enim",
    "description": "Quia eos sit suscipit. Autem libero delectus beatae. Iusto deleniti deleniti aspernatur est at distinctio laboriosam aut magni.",
    "status": "a",
    "time": "2055-08-25T17:34:44.608Z",
    "progressPer": 76,
    "type": "nesciunt",
    "isPined": "true",
    "users": [
        {
            "url": "http://placeimg.com/640/480"
        },
        {
            "url": "http://placeimg.com/640/480"
        },
        {
            "url": "http://placeimg.com/640/480"
        }
    ]
}
```

## Create a Kanban

**Description**

Create a kanban object.

**Parameters**

|name|type|description|
|---|---|---|
|id| long|Unique identifier for the object.|
|details| jsonb| Details for the object.|

**Return**

Returns the success status if the update succeeded. Returns an error if create parameters are invalid (e.g. specifying an invalid coupon or an invalid source).

**Curl Request**

    curl https://api.stripe.com/v1/customers \
    -u sk_test_4eC39HqLyjWDarjtT1zdp7dc: \
    -d description="My First Test Customer (created for API docs at https://www.stripe.com/docs/api)"

**Response**

```json   
{
    "code": 200,
    "message": "kanban added successfully",
    "type": "object",
    "object": []
}
```

## Update a Kanban

**Description**

Update a kanban object.

**Parameters**

|name|type|description|
|---|---|---|
|id| long|Unique identifier for the object.|
|details| jsonb| Details for the object.|

**Return**

Returns the success status if the update succeeded. Returns an error if create parameters are invalid (e.g. specifying an invalid coupon or an invalid source).

**Curl Request**

    curl https://api.stripe.com/v1/customers \
    -u sk_test_4eC39HqLyjWDarjtT1zdp7dc: \
    -d description="My First Test Customer (created for API docs at https://www.stripe.com/docs/api)"

**Response**

```json   
{
    "code": 200,
    "message": "kanban updated successfully",
    "type": "object",
    "object": []
}
```

## Delete a Kanban

**Description**

Delete a kanban object.

**Parameters**

|name|type|description|
|---|---|---|
|id| long|Unique identifier for the object.|
|details| jsonb| Details for the object.|

**Return**

Returns the success status if the update succeeded. Returns an error if create parameters are invalid (e.g. specifying an invalid coupon or an invalid source).

**Curl Request**

    curl https://api.stripe.com/v1/customers \
    -u sk_test_4eC39HqLyjWDarjtT1zdp7dc: \
    -d description="My First Test Customer (created for API docs at https://www.stripe.com/docs/api)"

**Response**

```json   
{
    "code": 200,
    "message": "kanban deleted successfully",
    "type": "object",
    "object": []
}
```

## Deactivate a Kanban

**Description**

Deactivate a kanban object.

**Parameters**

|name|type|description|
|---|---|---|
|id| long|Unique identifier for the object.|
|details| jsonb| Details for the object.|

**Return**

Returns the success status if the update succeeded. Returns an error if create parameters are invalid (e.g. specifying an invalid coupon or an invalid source).

**Curl Request**

    curl https://api.stripe.com/v1/customers \
    -u sk_test_4eC39HqLyjWDarjtT1zdp7dc: \
    -d description="My First Test Customer (created for API docs at https://www.stripe.com/docs/api)"

**Response**

```json   
{
    "code": 200,
    "message": "kanban deactivated successfully",
    "type": "object",
    "object": []
}
```

## Search Kanban

**Description**

Search a kanban object.

**Parameters**

|name|type|description|
|---|---|---|
|id| long|Unique identifier for the object.|
|details| jsonb| Details for the object.|

**Return**

Returns the success status if the update succeeded. Returns an error if create parameters are invalid (e.g. specifying an invalid coupon or an invalid source).

**Curl Request**

    curl https://api.stripe.com/v1/customers \
    -u sk_test_4eC39HqLyjWDarjtT1zdp7dc: \
    -d description="My First Test Customer (created for API docs at https://www.stripe.com/docs/api)"

**Response**

```json   
{
    "code": 200,
    "message": "kanban search successfully",
    "type": "object",
    "object": [*Array of resultant objects*]
}
```