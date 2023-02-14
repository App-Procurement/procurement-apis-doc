# Purchase Request

<table><thead><tr><th>Purchase Request</th><th>Endpoints</th><th data-hidden></th></tr></thead><tbody><tr><td>This object represents a customer of your business. It lets you create recurring charges and track payments that belong to the same customer.</td><td><a href="https://stripe.com/docs/api/customers#create_customer">  POST /v1/customers</a><a href="https://stripe.com/docs/api/customers#retrieve_customer">   GET /v1/customers/:id</a><a href="https://stripe.com/docs/api/customers#update_customer">  POST /v1/customers/:id</a><a href="https://stripe.com/docs/api/customers#delete_customer">DELETE /v1/customers/:id</a><a href="https://stripe.com/docs/api/customers#list_customers">   GET /v1/customers</a><a href="https://stripe.com/docs/api/customers#search_customers">   GET /v1/customers/search</a></td><td></td></tr></tbody></table>

## The Purchase Request Object

| Attributes                                                                                                                                            | The Purchase Request Object                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| ----------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <ul><li>id   string</li></ul><p>      Unique identifier for the object.</p><ul><li><h4>address      hash</h4><p>The customer’s address.</p></li></ul> | <pre class="language-json"><code class="lang-json">{
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
</code></pre> |

## Create a Purchase Request

## Update a Purchase Request

## Delete a Purchase Request

## Approve a Purchase Request

## Reject a Purchase Request

## List All Purchase Requests

## Search Purchase Requests
