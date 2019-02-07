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
#### Response:
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
			"img" : "this is the picture",
			"province" : "beijing",
			 "shop" : "the CHINA best shop"

}
		
]
}
```


## Cart
### List Cart
>GET /api/user/v1/cart
####Response:
```
{
		"code" : 0,
		"message" : "success",
		"data" : [
			{
			"cart_id" : 1,
			"img" : "this is the picture",
			"description" : "my shop is the best",
			"contunt" : 5,
			"price" : "585RMB",
			"move-favorite" : "move-favorite,
			"delete" : "delete" 
}
	
]

}

```
#### add count:
```
{
		"data" :[
				{
	count++;
}
]
}
```

#### reduce count:
```
{
		"data" : [
		{
			if(contunt>1){
		count--;
}if( contunt = 1){
		delete(cart);
}
}
]
}

```



## Order
### List Order
>GET /api/user/v1/order
####Response:
```
{
	"code" : 0,
	"message" : "success",
	"data" : [
		{
		"order_id" : 1,
		"List Product" : "List Product",
		"status": "status"
}
]
}
```
####upaid
```
{
	"data" : [
		{
		"order_id" : 1,
		"payment" : "payment",
		"price" : "55RMB",
		"cancel" : "cancel"
}
]
}
```

####paid
```
		{
			"data" :[
	{
		"order_id" : 1,
		"ship-status" : "ship-status",
		"cancel" : "cancel"
}
]
}
```

# Admin API
##ship
###ship-status
>GET /api/admin/v2/shippong
#####Response:
```
{
	"code" : 0,
	"message" : "success",
	"data" : [
{
		"order_id" : 1,
		"ship_id" : 1,
		"img" : "ding wei"
}
]
}
```



##Payment
###Payment-List
```
{
		"data" :[
	{
		"type": "wechat",
		"status" : "paid"
}

]
}
```
