# User API
## Product
### List Product

> GET /api/user/v1/products

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
            "price" : 1000,
            "img" : "http://www.ss.com"
        }
		
    ]
}

```

### Product Details

> GET /api/user/v1/product/[productId]

#### Response:
```
{
        "code" : 0,
		"message" : "success",
		"data":[
			{
            "product_id" : 1,
            "name" : "MeiZu mobile",
            "description" : "this is the product",
            "price" : 2000,
            "img" : "https://item.jd.com/1238332.html"
            "sku" : [
                  {
                    "sku_id" : 1,
                    "province" : "HeNan",
                    "color" : "blue",
                    "edition" : "MagBlue" 
                {
                    {
                    "sku_id" : 2,
                    "province" : "XiZang",
                    "color" : "red",
                    "edition" : " MagBlack"  
                 }
             ]
            }
		
      ]
}
```



## Cart
### List Cart

> GET /api/user/v1/cart

#### Response:

```
{
		"code" : 0,
		"message" : "success",
		"data" : [
			{
            "user_id" ; 1,
            "product_id" : 1,
            "sku_id" : 1,
            "cart_id" : 1,
            "img" : "https://item.jd.com/5089253.html#crumb-wrap",
            "description" : "MEIZU mobile",
            "contunt" : 1,
            "price" : 500 ,
            "select-count-status" : 1,
            "select-total-amount" : 500
           }
	
      ]

}
```


#### delete-cart

> DELETE /api/user/v1/cart/[cartId]

```
{
        "code" : 0,
        "message" : "success"
}
```

#### cart-product-number-management

> POST /api/user/v1/cart

```
{
         "code" : 0,
         "message" : "success",
         "data" : [
           
               {
                    "user_id" : 1,
                    "cart_id" : 1,
                    "sku_id" : 1,
                    "product_id" : 1,
                    "selete_item_count" : 2,
                    "total_price" : 500
                }
         
         ]

}

```

> PATCH /api/user/v1/cart/[cartId]

####  Response:
```
{
           "code" : 0,
           "message" : "success",
           "data" : [
                 {
                      "user_id" : 1,
                      "cart_id" : 1,
                      "product_id" :1,
                      "sku_id" : 1,
                      "selete_item_count" : 1,
                }
           
        ]
}

```




## Order
### List Order

> GET /api/user/v1/order

#### Response:
```
{
	"code" : 0,
	"message" : "success",
	"data" : [
		{
        "order_id" : 1,
        "product_id" : 1,
        "sku_id" : 1,
        "order_no" : 15664646,
        "status": 10,
        "postage" : 5000,
        "payment_type" : 1,
        "payment" : 100
       }
    ]
}
```

### cancel-order

> DELETE /api/user/v1/order/[order]

#### Response: 
```  
{
       "code" : 0,
       "message" : "success"    
    
}


```



### upaid-order
```
{
	"data" : [
		{
        "order_id" : 1,
        "order_no" : 5456464,
        "product_id" : 1,
        "user_id" : 1,
        "payment" : 222,
        "payment_type" : 1,
        "status" : 10
       }
   ]
}
```

### paying-order
```
		{
             "data" :[
	      {
             "user_id" : 1,
             "order_id" : 1,
             "product" : 1,
             "sku_id" : 1,
             "payment" : 555,

         }
     ]
}

```

### view-the-logistics
```
{
                     "data" : [
                           {
                              
                              "order_id" :1,
                              "product-name" : "MEIZU mobile",
                              "tracking-number" : 121515656
                         }
             ]

}
```



### Confirmation-of-receipt

> DELETE /api/user/v1/order/[orderId]

#### Response
```
{
        "code" : 0,
        "message" : "success"
    
}

```

# Admin API
### order-management

> GET /api/admin/v2/order

```
{
           "code" : 0,
           "message" : "success",
           "data" : [
              {
               "user_id" : 1,
               "oder_id" : 1,
               "product_id" : 1,
               "sku_id" : 1,
               "payment" : 5552,
               "name" : "MEIZU mobile",
               "description" : "blue",
               "status" : "paying"
                    
            } 
                
     ]
    
    
}

```

> DELETE /api/admin/v1/order
```
{
            "code" : 0,
            "message" : "success"


}
```


## stream
### stream-status

>GET /api/admin/v2/stream

#### Response:
```
{
	"code" : 0,
	"message" : "success",
	"data" : [
         {
           "order_id" : 1,
           "order_no" : 45456465,
           "stream_id" : 1,
           "stream-status" : "streaming", 
           "img" : "http://www.sss.com"
           "stream-address" : "xi'an" 
         }
    ]
}
```



## Payment
### Payment-List

> GET /api/admin/v1/payment

```
{
        "code" : 0 ,
        "message" : "success",
        "data" :[
	    {
            "pay_id" : 1,
            "type": 0,
            "status" : 1
      }
   ]
}
```

> DELETE /api/admin/v1/payment

#### Response

```
{
           "code" : 0,
           "message" : "success"
    
}

```
