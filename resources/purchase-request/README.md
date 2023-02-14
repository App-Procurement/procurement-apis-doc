# Purchase Request

This object represents the Purchase Requests that is raised from the internal employees of the organization to purchase any item.

**EndPoints**

    POST /v1/customers

    GET /v1/customers/:id

    POST /v1/customers/:id

    DELETE /v1/customers/:id

    GET /v1/customers

    GET /v1/customers/search
## The Purchase Request Object

**Attributes**

|name|type|description|
|---|---|---|
|id| string|Unique identifier for the object.|
|address| hash| The customer’s address.|

**The Object**

```json    
{
  "id": "cus_4QFOF3xrvBT2nU",
  "object": "customer",
  "address": {
    "city": "Cityd7ee8183-f31e-47ac-bcc0-dac0046e8267",
    "country": "Countrya0652216-3258-4103-a65d-4b20500a090b",
    "line1": "Line1b165233d-8c63-46f7-a685-a79abbbf4a03",
    "line2": "Line294d572f3-7624-40e4-ad04-621ea7ef07a2",
    "postal_code": "PostalCode4ae3bad5-65f4-413f-99ed-001d330ef5c5",
    "state": "State44125b42-ad62-4d3d-9d47-54ceecbbee1e"
  },
  "balance": 0,
  "created": 1405641986,
  "currency": "usd",
  "default_source": "card_14HOtJ2eZvKYlo2CD2lt4r4W",
  "delinquent": true,
  "description": "someone@example.com for Coderwall",
  "discount": null,
  "email": "name06849484-934c-45ef-88c1-0e7f9324699a@test.com",
  "invoice_prefix": "93EC0E1",
  "invoice_settings": {
    "custom_fields": null,
    "default_payment_method": null,
    "footer": null,
    "rendering_options": null
  },
  "livemode": false,
  "metadata": {
    "CustomerReferenceId": "16527612",
    "CustomerReferenceType": "reedonline",
    "tag-key": "tag-value",
    "meta-key": "meta-value",
    "order_id": "6735",
    "order_id_1": "6735",
    "email": "test@test.com",
    "adress": "testadress",
    "address": "testadress",
    "Address": "testadress"
  },
  "name": "name06849484-934c-45ef-88c1-0e7f9324699a",
  "next_invoice_sequence": 714223,
  "phone": null,
  "preferred_locales": [],
  "shipping": null,
  "tax_exempt": "none",
  "test_clock": null
}
```

## Create a Purchase Request

**Description**

Create a purchase request object for appproval of next lebel manager.

**Parameters**

|name|type|description|
|---|---|---|
|id| string|Unique identifier for the object.|
|address| hash| The customer’s address.|

**Return**

Returns the customer object if the update succeeded. Returns an error if create parameters are invalid (e.g. specifying an invalid coupon or an invalid source).

**Curl Request**

    curl https://api.stripe.com/v1/customers \
    -u sk_test_4eC39HqLyjWDarjtT1zdp7dc: \
    -d description="My First Test Customer (created for API docs at https://www.stripe.com/docs/api)"

**Response**

```json   
{
  "id": "cus_4QFOF3xrvBT2nU",
  "object": "customer",
  "address": {
    "city": "Cityd7ee8183-f31e-47ac-bcc0-dac0046e8267",
    "country": "Countrya0652216-3258-4103-a65d-4b20500a090b",
    "line1": "Line1b165233d-8c63-46f7-a685-a79abbbf4a03",
    "line2": "Line294d572f3-7624-40e4-ad04-621ea7ef07a2",
    "postal_code": "PostalCode4ae3bad5-65f4-413f-99ed-001d330ef5c5",
    "state": "State44125b42-ad62-4d3d-9d47-54ceecbbee1e"
  },
  "balance": 0,
  "created": 1405641986,
  "currency": "usd",
  "default_source": "card_14HOtJ2eZvKYlo2CD2lt4r4W",
  "delinquent": true,
  "description": "My First Test Customer (created for API docs at https://www.stripe.com/docs/api)",
  "discount": null,
  "email": "name06849484-934c-45ef-88c1-0e7f9324699a@test.com",
  "invoice_prefix": "93EC0E1",
  "invoice_settings": {
    "custom_fields": null,
    "default_payment_method": null,
    "footer": null,
    "rendering_options": null
  },
  "livemode": false,
  "metadata": {
    "CustomerReferenceId": "16527612",
    "CustomerReferenceType": "reedonline",
    "tag-key": "tag-value",
    "meta-key": "meta-value",
    "order_id": "6735",
    "order_id_1": "6735",
    "email": "test@test.com",
    "adress": "testadress",
    "address": "testadress",
    "Address": "testadress"
  },
  "name": "name06849484-934c-45ef-88c1-0e7f9324699a",
  "next_invoice_sequence": 714223,
  "phone": null,
  "preferred_locales": [],
  "shipping": null,
  "tax_exempt": "none",
  "test_clock": null
}
```

## Update a Purchase Request

## Delete a Purchase Request

## Approve a Purchase Request

## Reject a Purchase Request

## List All Purchase Requests

## Search Purchase Requests
