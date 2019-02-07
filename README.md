# User API
## Product
### List Product
>GET /api/user/v1/products
#### Response:
```
{
    "code": 0,
    "message": "success",
    "data": [
        {
            "product_id": 1,
            "name": "phone",
	    "description" : "miaoshu",
	    "price" : "RMB"
        }
		
    ]
}
```

### Details Product
>GET /api/user/v1/products-details
### Response:
```
{
		"code" : 0,
		"message" : "success",
		"data":[
			{
			"sku_id" : 1,
			"name" : "product",
			"description" : "this is the product",
			"price" : "10RMB",
			"img" : "this is the picture"
}
		
]
}
```
