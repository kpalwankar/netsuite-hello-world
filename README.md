# netsuite-order-api-mule4

# This is a simple Netsuite Order API built in Mule 4.

##### Use this API to: 
- Create a Sales Order 
- Read a Sales Order 
- Update a Sales Order
- Delete a Sales Order

### Create a Sales Order
`POST /api/orders` with the following body:
```
{
	"customerId": 534,
	"amount": 422.10,
	"quantity": 77
}
```

### Read a Sales Order
`GET /api/orders/{orderId}`
Response will look like the following if successful:
```
{
    "orderStatus": "PENDING_FULFILLMENT",
    "orderId": "88139",
    "quantity": 2,
    "total": 888.36,
    "email": "MLowdermilk@ecommerce4entrepreneurs.com",
    "shippingAddress": {
        "city": "Philadelphia",
        "country": "UNITED_STATES",
        "state": "PA",
        "zip": "18241",
        "addr1": "123 Test St"
    },
    "billingAddress": {
        "city": "Philadelphia",
        "country": "UNITED_STATES",
        "state": "PA",
        "zip": "18241",
        "addr1": "123 Test St"
    },
    "customerId": "534",
    "customerName": "Brick Metal Fabricators Services",
    "status": "Pending Fulfillment"
}
```

### Update a Sales Order
`PUT /api/orders/{orderId}` with the following body:
```
{
	"customerId": 534,
	"amount": 422.10,
	"quantity": 77
}
```

### Delete a Sales Order
`DELETE /api/orders/{orderId}`
Response will look like the following if successful:
```
{
    "status": "Order Deleted",
    "orderId": "86838"
}
```

