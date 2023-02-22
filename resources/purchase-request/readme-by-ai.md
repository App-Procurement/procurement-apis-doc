## Project Name: Procurement API

### Base URL

```
api.procurement.synectiks.net
```



Here's a list of APIs with endpoints for each entity you mentioned:

1. Kanban API
- POST /kanban
- PUT /kanban/:id
- DELETE /kanban/:id
- POST /kanban/deactivate/:id
- POST /kanban/approve/:id
- GET /kanban

2. Notification API
- POST /notification
- PUT /notification/:id
- DELETE /notification/:id
- POST /notification/deactivate/:id
- GET /notification

3. Contact API
- POST /contact
- PUT /contact/:id
- DELETE /contact/:id
- POST /contact/deactivate/:id
- GET /contact

4. Department API
- POST /department
- PUT /department/:id
- DELETE /department/:id
- POST /department/deactivate/:id
- GET /department

5. Company Profile API
- POST /company_profile
- PUT /company_profile/:id
- DELETE /company_profile/:id
- POST /company_profile/deactivate/:id
- GET /company_profile

6. Approvers API
- POST /approvers
- PUT /approvers/:id
- DELETE /approvers/:id
- POST /approvers/deactivate/:id
- POST /approvers/approve/:id
- GET /approvers

7. Quotation API
- POST /quotation
- PUT /quotation/:id
- DELETE /quotation/:id
- POST /quotation/deactivate/:id
- GET /quotation

8. Purchase Order API
- POST /purchase_order
- PUT /purchase_order/:id
- DELETE /purchase_order/:id
- POST /purchase_order/deactivate/:id
- GET /purchase_order

9. Invoice API
- POST /invoice
- PUT /invoice/:id
- DELETE /invoice/:id
- POST /invoice/deactivate/:id
- GET /invoice

10. Currency API
- POST /currency
- PUT /currency/:id
- DELETE /currency/:id
- POST /currency/deactivate/:id
- GET /currency

11. Product API
- POST /product
- PUT /product/:id
- DELETE /product/:id
- POST /product/deactivate/:id
- GET /product

12. Request API
- POST /request
- PUT /request/:id
- DELETE /request/:id
- POST /request/deactivate/:id
- POST /request/approve/:id
- GET /request



### Entity: Request

```json
{
    "id": 1,
    "details": {
        "createdBy": "requester id",
        "createdOn": "01-01-2022",
        "updatedBy": "updater name",
        "updatedOn": "01-01-2022",
        "approvedBy": [
            "approverId1",
            "approverId2",
            "approverId3"
        ],
        "approvedOn": "01-01-2022",
        "desiredDate": "01-01-2022",
        "location": "head office",
        "requestType": "purchase",
        "note": "This is note",
        "status": "active",
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
        "comments": [
            {
                "commentBy": "jitin",
                "commentOn": "12:00 12-12-1212",
                "comment": "this is new comment on this request"
            },
            {
                "commentBy": "jasmin",
                "commentOn": "12:00 12-12-1212",
                "comment": "this is new comment on this request"
            }
        ],
        "products": [
            {
                "item": {
                    "id": 3,
                    "details": {
                        "itemName": "mouse",
                        "itemType": "product",
                        "unit": "each",
                        "category": "tech",
                        "price": 12,
                        "imgUrl": "http://imgSynectiks.com",
                        "status": "ACTIVE"
                    }
                },
                "quantity": 1
            },
            {
                "item": {
                    "id": 2,
                    "details": {
                        "itemName": "hp laptop",
                        "itemType": "product",
                        "unit": "each",
                        "category": "tech",
                        "price": 800,
                        "imgUrl": "http://imgSynectiks.com",
                        "status": "ACTIVE"
                    }
                },
                "quantity": 1
            }
        ]
    }
}
```

#### Fields

| Field   | Type   | Description       |
|---------|--------|-------------------|
| id      | long   | Unique identifier |
| details | jsonb  | Request details   |

### Endpoints

#### `POST /request`

Create a new request.

##### Request

| Field   | Type   | Required | Description       |
|---------|--------|----------|-------------------|
| details | object | Yes      | Request details   |

##### Response

| Status code | Description        | Response body                         |
|-------------|--------------------|---------------------------------------|
| 200         | Success            | `{ "id": 1, "details": {} }`           |
| 400         | Bad request        | `{ "error": "Bad Request" }`          |

##### Example CURL

```
curl -X POST -H "Content-Type: application/json" -d '{"details": {}}' https://api.procurement.synectiks.net/request
```

#### `PUT /request/:id`

Update an existing request.

##### Request

| Field   | Type   | Required | Description       |
|---------|--------|----------|-------------------|
| details | object | Yes      | Request details   |

##### Response

| Status code | Description        | Response body                         |
|-------------|--------------------|---------------------------------------|
| 200         | Success            | `{ "id": 1, "details": {} }`           |
| 400         | Bad request        | `{ "error": "Bad Request" }`          |
| 404         | Request not found | `{ "error": "Request not found" }`    |

##### Example CURL

```
curl -X PUT -H "Content-Type: application/json" -d '{"details": {}}' https://api.procurement.synectiks.net/request/1
```

#### `DELETE /request/:id`

Delete a request.

##### Response

| Status code | Description        | Response body        |
|-------------|--------------------|----------------------|
| 200         | Success            | `{ "message": "OK" }` |
| 404         | Request not found | `{ "error": "Request not found" }` |

##### Example CURL

```
curl -X DELETE https://api.procurement.synectiks.net/request/1
```

#### `POST /request/deactivate/:id`

Deactivate a request.CURL
CURL
##### Response

| Status code | Description        | Response body        |
|-------------|--------------------|----------------------|
| 200         | Success            | `{ "message": "OK" }` |
| 404         | Request not found | `{ "error": "Request not found" }` |

##### Example CURL

```
curl -X POST https://api.procurement.synectiks.net/request/deactivate/1
```

#### `POST /request/approve/:id`

Approve a request.

##### Response

| Status code | Description        | Response body        |
|-------------|--------------------|----------------------|
| 200         | Success           




### Entity: product

```json
{
    "id": 1,
    "details": {
        "itemName": "mouse",
        "price": 12,
        "unit": "each",
        "itemType": "product",
        "category": "tech",
        "imgUrl": "http://imgSynectiks.com",
        "status":"ACTIVE"
        
    }
}
```


#### Fields

| Field   | Type   | Description       |
|---------|--------|-------------------|
| id      | long   | Unique identifier |
| details | jsonb  | product details   |

### Endpoints

#### `POST /product`

Create a new product.

##### product

| Field   | Type   | Required | Description       |
|---------|--------|----------|-------------------|
| details | object | Yes      | product details   |

##### Response

| Status code | Description        | Response body                         |
|-------------|--------------------|---------------------------------------|
| 200         | Success            | `{ "id": 1, "details": {} }`           |
| 400         | Bad product        | `{ "error": "Bad product" }`          |

##### Example CURL

```
curl -X POST -H "Content-Type: application/json" -d '{"details": {}}' https://api.procurement.synectiks.net/product
```

#### `PUT /product/:id`

Update an existing product.

##### product

| Field   | Type   | Required | Description       |
|---------|--------|----------|-------------------|
| details | object | Yes      | product details   |

##### Response

| Status code | Description        | Response body                         |
|-------------|--------------------|---------------------------------------|
| 200         | Success            | `{ "id": 1, "details": {} }`           |
| 400         | Bad product        | `{ "error": "Bad product" }`          |
| 404         | product not found | `{ "error": "product not found" }`    |

##### Example CURL

```
curl -X PUT -H "Content-Type: application/json" -d '{"details": {}}' https://api.procurement.synectiks.net/product/1
```

#### `DELETE /product/:id`

Delete a product.

##### Response

| Status code | Description        | Response body        |
|-------------|--------------------|----------------------|
| 200         | Success            | `{ "message": "OK" }` |
| 404         | product not found | `{ "error": "product not found" }` |

##### Example CURL

```
curl -X DELETE https://api.procurement.synectiks.net/product/1
```

#### `POST /product/deactivate/:id`

Deactivate a product.CURL
CURL
##### Response

| Status code | Description        | Response body        |
|-------------|--------------------|----------------------|
| 200         | Success            | `{ "message": "OK" }` |
| 404         | product not found | `{ "error": "product not found" }` |

##### Example CURL

```
curl -X POST https://api.procurement.synectiks.net/product/deactivate/1
```



### Entity: supplier

```json
{
    "id": 1,
    "details": {
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


#### Fields

| Field   | Type   | Description       |
|---------|--------|-------------------|
| id      | long   | Unique identifier |
| details | jsonb  | supplier details   |

### Endpoints

#### `POST /supplier`

Create a new supplier.

##### supplier

| Field   | Type   | Required | Description       |
|---------|--------|----------|-------------------|
| details | object | Yes      | supplier details   |

##### Response

| Status code | Description        | Response body                         |
|-------------|--------------------|---------------------------------------|
| 200         | Success            | `{ "id": 1, "details": {} }`           |
| 400         | Bad supplier        | `{ "error": "Bad supplier" }`          |

##### Example CURL

```
curl -X POST -H "Content-Type: application/json" -d '{"details": {}}' https://api.procurement.synectiks.net/supplier
```

#### `PUT /supplier/:id`

Update an existing supplier.

##### supplier

| Field   | Type   | Required | Description       |
|---------|--------|----------|-------------------|
| details | object | Yes      | supplier details   |

##### Response

| Status code | Description        | Response body                         |
|-------------|--------------------|---------------------------------------|
| 200         | Success            | `{ "id": 1, "details": {} }`           |
| 400         | Bad supplier        | `{ "error": "Bad supplier" }`          |
| 404         | supplier not found | `{ "error": "supplier not found" }`    |

##### Example CURL

```
curl -X PUT -H "Content-Type: application/json" -d '{"details": {}}' https://api.procurement.synectiks.net/supplier/1
```

#### `DELETE /supplier/:id`

Delete a supplier.

##### Response

| Status code | Description        | Response body        |
|-------------|--------------------|----------------------|
| 200         | Success            | `{ "message": "OK" }` |
| 404         | supplier not found | `{ "error": "supplier not found" }` |

##### Example CURL

```
curl -X DELETE https://api.procurement.synectiks.net/supplier/1
```

#### `POST /supplier/deactivate/:id`

Deactivate a supplier.CURL
CURL
##### Response

| Status code | Description        | Response body        |
|-------------|--------------------|----------------------|
| 200         | Success            | `{ "message": "OK" }` |
| 404         | supplier not found | `{ "error": "supplier not found" }` |

##### Example CURL

```
curl -X POST https://api.procurement.synectiks.net/supplier/deactivate/1
```



### Entity: currency

```json
{
    "id": 1,
    "details": {
        "code": "USD",
        "name": "doller",
        "countryName": "USA",
        "countryCode": 1,
        "status":"ACTIVE"
    }
}
```


#### Fields

| Field   | Type   | Description       |
|---------|--------|-------------------|
| id      | long   | Unique identifier |
| details | jsonb  | currency details   |

### Endpoints

#### `POST /currency`

Create a new currency.

##### currency

| Field   | Type   | Required | Description       |
|---------|--------|----------|-------------------|
| details | object | Yes      | currency details   |

##### Response

| Status code | Description        | Response body                         |
|-------------|--------------------|---------------------------------------|
| 200         | Success            | `{ "id": 1, "details": {} }`           |
| 400         | Bad currency        | `{ "error": "Bad currency" }`          |

##### Example CURL

```
curl -X POST -H "Content-Type: application/json" -d '{"details": {}}' https://api.procurement.synectiks.net/currency
```

#### `PUT /currency/:id`

Update an existing currency.

##### currency

| Field   | Type   | Required | Description       |
|---------|--------|----------|-------------------|
| details | object | Yes      | currency details   |

##### Response

| Status code | Description        | Response body                         |
|-------------|--------------------|---------------------------------------|
| 200         | Success            | `{ "id": 1, "details": {} }`           |
| 400         | Bad currency        | `{ "error": "Bad currency" }`          |
| 404         | currency not found | `{ "error": "currency not found" }`    |

##### Example CURL

```
curl -X PUT -H "Content-Type: application/json" -d '{"details": {}}' https://api.procurement.synectiks.net/currency/1
```

#### `DELETE /currency/:id`

Delete a currency.

##### Response

| Status code | Description        | Response body        |
|-------------|--------------------|----------------------|
| 200         | Success            | `{ "message": "OK" }` |
| 404         | currency not found | `{ "error": "currency not found" }` |

##### Example CURL

```
curl -X DELETE https://api.procurement.synectiks.net/currency/1
```

#### `POST /currency/deactivate/:id`

Deactivate a currency.CURL
CURL
##### Response

| Status code | Description        | Response body        |
|-------------|--------------------|----------------------|
| 200         | Success            | `{ "message": "OK" }` |
| 404         | currency not found | `{ "error": "currency not found" }` |

##### Example CURL

```
curl -X POST https://api.procurement.synectiks.net/currency/deactivate/1
```


### Entity: invoice

```json
{
    "id": 1,
    "details": {
        "url": "http://invoice-location.com",
        "issueDate": "15-01-2022",
        "invoiceDueDate": "15-01-2022",
        "amount": "824",
        "tax": "+18VAT",
        "status": "ACTIVE",
        "purchaseOrder": {
            "id": 1,
            "details": {
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
                "notes": "this is notes for Purchase Order",
                "supplier": {
                    "id": 1,
                    "details": {
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
                "requestsDetail": [
                    {
                        "requestId": 1,
                        "productIds": [
                            2,
                            3
                        ]
                    },
                    {
                        "requestId": 2,
                        "productIds": [
                            1,
                            2
                        ]
                    }
                ],
                "purchaseOrderProducts": [
                    {
                        "item": {
                            "id": 1,
                            "details": {
                                "itemName": "mouse",
                                "price": 12,
                                "unit": "each",
                                "itemType": "product",
                                "category": "tech",
                                "imgUrl": "http://imgSynectiks.com",
                                "status": "ACTIVE"
                            }
                        },
                        "quantity": 1
                    },
                    {
                        "item": {
                            "id": 2,
                            "details": {
                                "itemName": "hp laptop",
                                "itemType": "product",
                                "unit": "each",
                                "category": "tech",
                                "price": 800,
                                "imgUrl": "http://imgSynectiks.com",
                                "status": "ACTIVE"
                            }
                        },
                        "quantity": 2
                    }
                ]
            }
        },
        "currency": {
            "id": 1,
            "details": {
                "code": "USD",
                "Name": "doller",
                "countryName": "USA",
                "countryCode": "1"
            }
        }
    }
}
```


#### Fields

| Field   | Type   | Description       |
|---------|--------|-------------------|
| id      | long   | Unique identifier |
| details | jsonb  | invoice details   |

### Endpoints

#### `POST /invoice`

Create a new invoice.

##### invoice

| Field   | Type   | Required | Description       |
|---------|--------|----------|-------------------|
| details | object | Yes      | invoice details   |

##### Response

| Status code | Description        | Response body                         |
|-------------|--------------------|---------------------------------------|
| 200         | Success            | `{ "id": 1, "details": {} }`           |
| 400         | Bad invoice        | `{ "error": "Bad invoice" }`          |

##### Example CURL

```
curl -X POST -H "Content-Type: application/json" -d '{"details": {}}' https://api.procurement.synectiks.net/invoice
```

#### `PUT /invoice/:id`

Update an existing invoice.

##### invoice

| Field   | Type   | Required | Description       |
|---------|--------|----------|-------------------|
| details | object | Yes      | invoice details   |

##### Response

| Status code | Description        | Response body                         |
|-------------|--------------------|---------------------------------------|
| 200         | Success            | `{ "id": 1, "details": {} }`           |
| 400         | Bad invoice        | `{ "error": "Bad invoice" }`          |
| 404         | invoice not found | `{ "error": "invoice not found" }`    |

##### Example CURL

```
curl -X PUT -H "Content-Type: application/json" -d '{"details": {}}' https://api.procurement.synectiks.net/invoice/1
```

#### `DELETE /invoice/:id`

Delete a invoice.

##### Response

| Status code | Description        | Response body        |
|-------------|--------------------|----------------------|
| 200         | Success            | `{ "message": "OK" }` |
| 404         | invoice not found | `{ "error": "invoice not found" }` |

##### Example CURL

```
curl -X DELETE https://api.procurement.synectiks.net/invoice/1
```

#### `POST /invoice/deactivate/:id`

Deactivate a invoice.CURL
CURL
##### Response

| Status code | Description        | Response body        |
|-------------|--------------------|----------------------|
| 200         | Success            | `{ "message": "OK" }` |
| 404         | invoice not found | `{ "error": "invoice not found" }` |

##### Example CURL

```
curl -X POST https://api.procurement.synectiks.net/invoice/deactivate/1
```


### Entity: purchase_order

```json
{
    "id": 1,
    "details": {
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
        "notes": "this is notes for Purchase Order",
        "supplier": {
            "id": 1,
            "details": {
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
        "requestsDetail": [
            {
                "requestId": 1,
                "productIds": [
                    2,
                    3
                ]
            },
            {
                "requestId": 2,
                "productIds": [
                    1,
                    2
                ]
            }
        ],
        "purchaseOrderProducts": [
            {
                "item": {
                    "id": 1,
                    "details": {
                        "itemName": "mouse",
                        "price": 12,
                        "unit": "each",
                        "itemType": "product",
                        "category": "tech",
                        "imgUrl": "http://imgSynectiks.com",
                        "status": "ACTIVE"
                    }
                },
                "quantity": 1
            },
            {
                "item": {
                    "id": 2,
                    "details": {
                        "itemName": "hp laptop",
                        "itemType": "product",
                        "unit": "each",
                        "category": "tech",
                        "price": 800,
                        "imgUrl": "http://imgSynectiks.com",
                        "status": "ACTIVE"
                    }
                },
                "quantity": 2
            }
        ],
        "quotation": {
            "id": 1,
            "details": {
                "openDate": "01-01-2000",
                "closingDate": "01-01-2000",
                "requiredDeliveryDate": "01-01-2000",
                "rfqType": "demo",
                "location": "head office",
                "note": "this is note",
                "paymentTerms": "terms",
                "paymentMode": "ABCD",
                "incoterms": "ABCD",
                "modeOfDelivery": "accountHolderName",
                "status": "active",
                "requestsDetail": [
                    {
                        "requestId": 1,
                        "productIds": [
                            2,
                            3
                        ]
                    },
                    {
                        "requestId": 2,
                        "productIds": [
                            1,
                            2
                        ]
                    }
                ],
                "products": [
                    {
                        "item": {
                            "id": 1,
                            "details": {
                                "itemName": "mouse",
                                "price": 12,
                                "unit": "each",
                                "itemType": "product",
                                "category": "tech"
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
                            "category": "tech"
                        },
                        "quantity": 2
                    }
                ],
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
    }
}
```


#### Fields

| Field   | Type   | Description       |
|---------|--------|-------------------|
| id      | long   | Unique identifier |
| details | jsonb  | purchase_order details   |

### Endpoints

#### `POST /purchase_order`

Create a new purchase_order.

##### purchase_order

| Field   | Type   | Required | Description       |
|---------|--------|----------|-------------------|
| details | object | Yes      | purchase_order details   |

##### Response

| Status code | Description        | Response body                         |
|-------------|--------------------|---------------------------------------|
| 200         | Success            | `{ "id": 1, "details": {} }`           |
| 400         | Bad purchase_order        | `{ "error": "Bad purchase_order" }`          |

##### Example CURL

```
curl -X POST -H "Content-Type: application/json" -d '{"details": {}}' https://api.procurement.synectiks.net/purchase_order
```

#### `PUT /purchase_order/:id`

Update an existing purchase_order.

##### purchase_order

| Field   | Type   | Required | Description       |
|---------|--------|----------|-------------------|
| details | object | Yes      | purchase_order details   |

##### Response

| Status code | Description        | Response body                         |
|-------------|--------------------|---------------------------------------|
| 200         | Success            | `{ "id": 1, "details": {} }`           |
| 400         | Bad purchase_order        | `{ "error": "Bad purchase_order" }`          |
| 404         | purchase_order not found | `{ "error": "purchase_order not found" }`    |

##### Example CURL

```
curl -X PUT -H "Content-Type: application/json" -d '{"details": {}}' https://api.procurement.synectiks.net/purchase_order/1
```

#### `DELETE /purchase_order/:id`

Delete a purchase_order.

##### Response

| Status code | Description        | Response body        |
|-------------|--------------------|----------------------|
| 200         | Success            | `{ "message": "OK" }` |
| 404         | purchase_order not found | `{ "error": "purchase_order not found" }` |

##### Example CURL

```
curl -X DELETE https://api.procurement.synectiks.net/purchase_order/1
```

#### `POST /purchase_order/deactivate/:id`

Deactivate a purchase_order.CURL
CURL
##### Response

| Status code | Description        | Response body        |
|-------------|--------------------|----------------------|
| 200         | Success            | `{ "message": "OK" }` |
| 404         | purchase_order not found | `{ "error": "purchase_order not found" }` |

##### Example CURL

```
curl -X POST https://api.procurement.synectiks.net/purchase_order/deactivate/1
```


### Entity: quotation

```json
{
    "id": 1,
    "details": {
        "openDate": "01-01-2000",
        "closingDate": "01-01-2000",
        "requiredDeliveryDate": "01-01-2000",
        "rfqType": "demo",
        "location": "head office",
        "note": "this is note",
        "paymentTerms": "terms",
        "paymentMode": "ABCD",
        "incoterms": "ABCD",
        "modeOfDelivery": "accountHolderName",
        "status": "active",
        "requestsDetail": [
            {
                "requestId": 1,
                "productIds": [
                    2,
                    3
                ]
            },
            {
                "requestId": 2,
                "productIds": [
                    1,
                    2
                ]
            }
        ],
        "products": [
            {
                "item": {
                    "id": 1,
                    "details": {
                        "itemName": "mouse",
                        "price": 12,
                        "unit": "each",
                        "itemType": "product",
                        "category": "tech"
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
                    "category": "tech"
                },
                "quantity": 2
            }
        ],
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

#### Fields

| Field   | Type   | Description       |
|---------|--------|-------------------|
| id      | long   | Unique identifier |
| details | jsonb  | quotation details   |

### Endpoints

#### `POST /quotation`

Create a new quotation.

##### quotation

| Field   | Type   | Required | Description       |
|---------|--------|----------|-------------------|
| details | object | Yes      | quotation details   |

##### Response

| Status code | Description        | Response body                         |
|-------------|--------------------|---------------------------------------|
| 200         | Success            | `{ "id": 1, "details": {} }`           |
| 400         | Bad quotation        | `{ "error": "Bad quotation" }`          |

##### Example CURL

```
curl -X POST -H "Content-Type: application/json" -d '{"details": {}}' https://api.procurement.synectiks.net/quotation
```

#### `PUT /quotation/:id`

Update an existing quotation.

##### quotation

| Field   | Type   | Required | Description       |
|---------|--------|----------|-------------------|
| details | object | Yes      | quotation details   |

##### Response

| Status code | Description        | Response body                         |
|-------------|--------------------|---------------------------------------|
| 200         | Success            | `{ "id": 1, "details": {} }`           |
| 400         | Bad quotation        | `{ "error": "Bad quotation" }`          |
| 404         | quotation not found | `{ "error": "quotation not found" }`    |

##### Example CURL

```
curl -X PUT -H "Content-Type: application/json" -d '{"details": {}}' https://api.procurement.synectiks.net/quotation/1
```

#### `DELETE /quotation/:id`

Delete a quotation.

##### Response

| Status code | Description        | Response body        |
|-------------|--------------------|----------------------|
| 200         | Success            | `{ "message": "OK" }` |
| 404         | quotation not found | `{ "error": "quotation not found" }` |

##### Example CURL

```
curl -X DELETE https://api.procurement.synectiks.net/quotation/1
```

#### `POST /quotation/deactivate/:id`

Deactivate a quotation.CURL
CURL
##### Response

| Status code | Description        | Response body        |
|-------------|--------------------|----------------------|
| 200         | Success            | `{ "message": "OK" }` |
| 404         | quotation not found | `{ "error": "quotation not found" }` |

##### Example CURL

```
curl -X POST https://api.procurement.synectiks.net/quotation/deactivate/1
```


### Entity: approvers

```json
{
    "id": 1,
    "details": {
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
}
```


#### Fields

| Field   | Type   | Description       |
|---------|--------|-------------------|
| id      | long   | Unique identifier |
| details | jsonb  | approvers details   |

### Endpoints

#### `POST /approvers`

Create a new approvers.

##### approvers

| Field   | Type   | Required | Description       |
|---------|--------|----------|-------------------|
| details | object | Yes      | approvers details   |

##### Response

| Status code | Description        | Response body                         |
|-------------|--------------------|---------------------------------------|
| 200         | Success            | `{ "id": 1, "details": {} }`           |
| 400         | Bad approvers        | `{ "error": "Bad approvers" }`          |

##### Example CURL

```
curl -X POST -H "Content-Type: application/json" -d '{"details": {}}' https://api.procurement.synectiks.net/approvers
```

#### `PUT /approvers/:id`

Update an existing approvers.

##### approvers

| Field   | Type   | Required | Description       |
|---------|--------|----------|-------------------|
| details | object | Yes      | approvers details   |

##### Response

| Status code | Description        | Response body                         |
|-------------|--------------------|---------------------------------------|
| 200         | Success            | `{ "id": 1, "details": {} }`           |
| 400         | Bad approvers        | `{ "error": "Bad approvers" }`          |
| 404         | approvers not found | `{ "error": "approvers not found" }`    |

##### Example CURL

```
curl -X PUT -H "Content-Type: application/json" -d '{"details": {}}' https://api.procurement.synectiks.net/approvers/1
```

#### `DELETE /approvers/:id`

Delete a approvers.

##### Response

| Status code | Description        | Response body        |
|-------------|--------------------|----------------------|
| 200         | Success            | `{ "message": "OK" }` |
| 404         | approvers not found | `{ "error": "approvers not found" }` |

##### Example CURL

```
curl -X DELETE https://api.procurement.synectiks.net/approvers/1
```

#### `POST /approvers/deactivate/:id`

Deactivate a approvers.CURL
CURL
##### Response

| Status code | Description        | Response body        |
|-------------|--------------------|----------------------|
| 200         | Success            | `{ "message": "OK" }` |
| 404         | approvers not found | `{ "error": "approvers not found" }` |

##### Example CURL

```
curl -X POST https://api.procurement.synectiks.net/approvers/deactivate/1
```


### Entity: company_profile

```json
{
    "id": 1,
    "details": {
        "accountHolderName": "this is name",
        "companyName": "company",
        "country": "country",
        "state": "state",
        "emailAddress": "email@email.com",
        "contactNo": "987654321",
        "date": "01-01-1000",
        "address": "address"
    }
}
```


#### Fields

| Field   | Type   | Description       |
|---------|--------|-------------------|
| id      | long   | Unique identifier |
| details | jsonb  | company_profile details   |

### Endpoints

#### `POST /company_profile`

Create a new company_profile.

##### company_profile

| Field   | Type   | Required | Description       |
|---------|--------|----------|-------------------|
| details | object | Yes      | company_profile details   |

##### Response

| Status code | Description        | Response body                         |
|-------------|--------------------|---------------------------------------|
| 200         | Success            | `{ "id": 1, "details": {} }`           |
| 400         | Bad company_profile        | `{ "error": "Bad company_profile" }`          |

##### Example CURL

```
curl -X POST -H "Content-Type: application/json" -d '{"details": {}}' https://api.procurement.synectiks.net/company_profile
```

#### `PUT /company_profile/:id`

Update an existing company_profile.

##### company_profile

| Field   | Type   | Required | Description       |
|---------|--------|----------|-------------------|
| details | object | Yes      | company_profile details   |

##### Response

| Status code | Description        | Response body                         |
|-------------|--------------------|---------------------------------------|
| 200         | Success            | `{ "id": 1, "details": {} }`           |
| 400         | Bad company_profile        | `{ "error": "Bad company_profile" }`          |
| 404         | company_profile not found | `{ "error": "company_profile not found" }`    |

##### Example CURL

```
curl -X PUT -H "Content-Type: application/json" -d '{"details": {}}' https://api.procurement.synectiks.net/company_profile/1
```

#### `DELETE /company_profile/:id`

Delete a company_profile.

##### Response

| Status code | Description        | Response body        |
|-------------|--------------------|----------------------|
| 200         | Success            | `{ "message": "OK" }` |
| 404         | company_profile not found | `{ "error": "company_profile not found" }` |

##### Example CURL

```
curl -X DELETE https://api.procurement.synectiks.net/company_profile/1
```

#### `POST /company_profile/deactivate/:id`

Deactivate a company_profile.CURL
CURL
##### Response

| Status code | Description        | Response body        |
|-------------|--------------------|----------------------|
| 200         | Success            | `{ "message": "OK" }` |
| 404         | company_profile not found | `{ "error": "company_profile not found" }` |

##### Example CURL

```
curl -X POST https://api.procurement.synectiks.net/company_profile/deactivate/1
```


### Entity: department

```json
{
    "id": 1,
    "details": {
        "name": "toys",
        "status": "ACTIVE"
    }
}
```


#### Fields

| Field   | Type   | Description       |
|---------|--------|-------------------|
| id      | long   | Unique identifier |
| details | jsonb  | department details   |

### Endpoints

#### `POST /department`

Create a new department.

##### department

| Field   | Type   | Required | Description       |
|---------|--------|----------|-------------------|
| details | object | Yes      | department details   |

##### Response

| Status code | Description        | Response body                         |
|-------------|--------------------|---------------------------------------|
| 200         | Success            | `{ "id": 1, "details": {} }`           |
| 400         | Bad department        | `{ "error": "Bad department" }`          |

##### Example CURL

```
curl -X POST -H "Content-Type: application/json" -d '{"details": {}}' https://api.procurement.synectiks.net/department
```

#### `PUT /department/:id`

Update an existing department.

##### department

| Field   | Type   | Required | Description       |
|---------|--------|----------|-------------------|
| details | object | Yes      | department details   |

##### Response

| Status code | Description        | Response body                         |
|-------------|--------------------|---------------------------------------|
| 200         | Success            | `{ "id": 1, "details": {} }`           |
| 400         | Bad department        | `{ "error": "Bad department" }`          |
| 404         | department not found | `{ "error": "department not found" }`    |

##### Example CURL

```
curl -X PUT -H "Content-Type: application/json" -d '{"details": {}}' https://api.procurement.synectiks.net/department/1
```

#### `DELETE /department/:id`

Delete a department.

##### Response

| Status code | Description        | Response body        |
|-------------|--------------------|----------------------|
| 200         | Success            | `{ "message": "OK" }` |
| 404         | department not found | `{ "error": "department not found" }` |

##### Example CURL

```
curl -X DELETE https://api.procurement.synectiks.net/department/1
```

#### `POST /department/deactivate/:id`

Deactivate a department.CURL
CURL
##### Response

| Status code | Description        | Response body        |
|-------------|--------------------|----------------------|
| 200         | Success            | `{ "message": "OK" }` |
| 404         | department not found | `{ "error": "department not found" }` |

##### Example CURL

```
curl -X POST https://api.procurement.synectiks.net/department/deactivate/1
```


### Entity: contact

```json
{
    "id": 1,
    "details": {
        "company": "Klein, Dach and Zulauf",
        "email": "Noah78@hotmail.com",
        "name": "Doyle Hand",
        "position": "Ergonomic reciprocal definition",
        "profile": "http://placeimg.com/640/480",
        "contNo": 1580330181,
        "status": "ACTIVE"
    }
}
```

#### Fields

| Field   | Type   | Description       |
|---------|--------|-------------------|
| id      | long   | Unique identifier |
| details | jsonb  | contact details   |

### Endpoints

#### `POST /contact`

Create a new contact.

##### contact

| Field   | Type   | Required | Description       |
|---------|--------|----------|-------------------|
| details | object | Yes      | contact details   |

##### Response

| Status code | Description        | Response body                         |
|-------------|--------------------|---------------------------------------|
| 200         | Success            | `{ "id": 1, "details": {} }`           |
| 400         | Bad contact        | `{ "error": "Bad contact" }`          |

##### Example CURL

```
curl -X POST -H "Content-Type: application/json" -d '{"details": {}}' https://api.procurement.synectiks.net/contact
```

#### `PUT /contact/:id`

Update an existing contact.

##### contact

| Field   | Type   | Required | Description       |
|---------|--------|----------|-------------------|
| details | object | Yes      | contact details   |

##### Response

| Status code | Description        | Response body                         |
|-------------|--------------------|---------------------------------------|
| 200         | Success            | `{ "id": 1, "details": {} }`           |
| 400         | Bad contact        | `{ "error": "Bad contact" }`          |
| 404         | contact not found | `{ "error": "contact not found" }`    |

##### Example CURL

```
curl -X PUT -H "Content-Type: application/json" -d '{"details": {}}' https://api.procurement.synectiks.net/contact/1
```

#### `DELETE /contact/:id`

Delete a contact.

##### Response

| Status code | Description        | Response body        |
|-------------|--------------------|----------------------|
| 200         | Success            | `{ "message": "OK" }` |
| 404         | contact not found | `{ "error": "contact not found" }` |

##### Example CURL

```
curl -X DELETE https://api.procurement.synectiks.net/contact/1
```

#### `POST /contact/deactivate/:id`

Deactivate a contact.CURL
CURL
##### Response

| Status code | Description        | Response body        |
|-------------|--------------------|----------------------|
| 200         | Success            | `{ "message": "OK" }` |
| 404         | contact not found | `{ "error": "contact not found" }` |

##### Example CURL

```
curl -X POST https://api.procurement.synectiks.net/contact/deactivate/1
```


### Entity: notification

```json
{
    "id": 1,
    "details": {
        "title": "Milan.Braun20",
        "img": "http://placeimg.com/640/480",
        "description": "sequi",
        "status": "ACTIVE"
    }
}

```


#### Fields

| Field   | Type   | Description       |
|---------|--------|-------------------|
| id      | long   | Unique identifier |
| details | jsonb  | notification details   |

### Endpoints

#### `POST /notification`

Create a new notification.

##### notification

| Field   | Type   | Required | Description       |
|---------|--------|----------|-------------------|
| details | object | Yes      | notification details   |

##### Response

| Status code | Description        | Response body                         |
|-------------|--------------------|---------------------------------------|
| 200         | Success            | `{ "id": 1, "details": {} }`           |
| 400         | Bad notification        | `{ "error": "Bad notification" }`          |

##### Example CURL

```
curl -X POST -H "Content-Type: application/json" -d '{"details": {}}' https://api.procurement.synectiks.net/notification
```

#### `PUT /notification/:id`

Update an existing notification.

##### notification

| Field   | Type   | Required | Description       |
|---------|--------|----------|-------------------|
| details | object | Yes      | notification details   |

##### Response

| Status code | Description        | Response body                         |
|-------------|--------------------|---------------------------------------|
| 200         | Success            | `{ "id": 1, "details": {} }`           |
| 400         | Bad notification        | `{ "error": "Bad notification" }`          |
| 404         | notification not found | `{ "error": "notification not found" }`    |

##### Example CURL

```
curl -X PUT -H "Content-Type: application/json" -d '{"details": {}}' https://api.procurement.synectiks.net/notification/1
```

#### `DELETE /notification/:id`

Delete a notification.

##### Response

| Status code | Description        | Response body        |
|-------------|--------------------|----------------------|
| 200         | Success            | `{ "message": "OK" }` |
| 404         | notification not found | `{ "error": "notification not found" }` |

##### Example CURL

```
curl -X DELETE https://api.procurement.synectiks.net/notification/1
```

#### `POST /notification/deactivate/:id`

Deactivate a notification.CURL
CURL
##### Response

| Status code | Description        | Response body        |
|-------------|--------------------|----------------------|
| 200         | Success            | `{ "message": "OK" }` |
| 404         | notification not found | `{ "error": "notification not found" }` |

##### Example CURL

```
curl -X POST https://api.procurement.synectiks.net/notification/deactivate/1
```


### Entity: kanban

```json
{
    "id": 1,
    "details": {
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
}
```


#### Fields

| Field   | Type   | Description       |
|---------|--------|-------------------|
| id      | long   | Unique identifier |
| details | jsonb  | kanban details   |

### Endpoints

#### `POST /kanban`

Create a new kanban.

##### kanban

| Field   | Type   | Required | Description       |
|---------|--------|----------|-------------------|
| details | object | Yes      | kanban details   |

##### Response

| Status code | Description        | Response body                         |
|-------------|--------------------|---------------------------------------|
| 200         | Success            | `{ "id": 1, "details": {} }`           |
| 400         | Bad kanban        | `{ "error": "Bad kanban" }`          |

##### Example CURL

```
curl -X POST -H "Content-Type: application/json" -d '{"details": {}}' https://api.procurement.synectiks.net/kanban
```

#### `PUT /kanban/:id`

Update an existing kanban.

##### kanban

| Field   | Type   | Required | Description       |
|---------|--------|----------|-------------------|
| details | object | Yes      | kanban details   |

##### Response

| Status code | Description        | Response body                         |
|-------------|--------------------|---------------------------------------|
| 200         | Success            | `{ "id": 1, "details": {} }`           |
| 400         | Bad kanban        | `{ "error": "Bad kanban" }`          |
| 404         | kanban not found | `{ "error": "kanban not found" }`    |

##### Example CURL

```
curl -X PUT -H "Content-Type: application/json" -d '{"details": {}}' https://api.procurement.synectiks.net/kanban/1
```

#### `DELETE /kanban/:id`

Delete a kanban.

##### Response

| Status code | Description        | Response body        |
|-------------|--------------------|----------------------|
| 200         | Success            | `{ "message": "OK" }` |
| 404         | kanban not found | `{ "error": "kanban not found" }` |

##### Example CURL

```
curl -X DELETE https://api.procurement.synectiks.net/kanban/1
```

#### `POST /kanban/deactivate/:id`

Deactivate a kanban.CURL
CURL
##### Response

| Status code | Description        | Response body        |
|-------------|--------------------|----------------------|
| 200         | Success            | `{ "message": "OK" }` |
| 404         | kanban not found | `{ "error": "kanban not found" }` |

##### Example CURL

```
curl -X POST https://api.procurement.synectiks.net/kanban/deactivate/1
```

