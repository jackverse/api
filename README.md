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
