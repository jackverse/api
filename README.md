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

### Product Details
>GET /api/user/v1/product/1
#### Response:
```
{
        "code" : 0,
		"message" : "success",
		"data":[
			{
            "product_id" : 1,
			"sku_id" : 1,
			"name" : "MeiZu mobile",
			"description" : "this is the product",
			"price" : 2000,
			"img" : "https://item.jd.com/1238332.html",
			"province" : "beijing",
            "color" : "blue" 

            }
		
      ]
}
```

#### Sku Classify
>GET /api/user/v1/sku/2
#### Response:
```
{
            "code" : 0 ,
            "message" : "success",
            "data" : [
              {
                  "product_id" : 1 , 
                  "sku_id" : 1 ,
                  "name" : "MeiZu mobile",
                  "description" : "MeiZu Red mobile",
                  "price" : 2500,
                  "img" : "https://item.jd.com/5089253.html#crumb-wrap",
                  "province" : "beijing",
                  "color" : "red"
            }
        ]
}


```

#### Add Product
```
{
            "data" : [
            {
                "count" : 1,
                count++      
                
                
            }
            
        ]    
}
```

#### Reduce Product
```
{
            "data" : [
                 {
                 if(count = 1){
                             return null;       
                                
                            }
                    if(count > 1) {
                             count--;
                        }
              }            
        ]
}

```



## Cart
### List Cart
>GET /api/user/v1/cart
#### Response:
```
{
		"code" : 0,
		"message" : "success",
		"data" : [
			{
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
		"data" :  [
	         	 {
			if(contunt>1){
		                   count--;
                         }if( contunt = 1){
		                            return null;
                                }
                }
        ]
}

```

#### delete product
```

{
            "data" : [
                  {
                      delete(product);            
                    
                }
            
        ]
}
```




#### select count
```
{
	"data" :    [ 
              {
		           if(select-count-status=1){
                        
                          select-total-amount= select-total-amount + price;
                       }if(select-count-status=0){
                           
                             select-toal-amount = select-total-amount + 0 ;
                           }


            }

      ]

}



```

#### settle accounts
```
{
         "data" [
         
                        {
                           order        
                    }
         
         
         ]    
    
}

```






## Order
### List Order
>GET /api/user/v1/order
#### Response:
```
{
	"code" : 0,
	"message" : "success",
	"data" : [
		{
		"order_id" : 1,
		"product_id" : 1,
		"order-status": "upaid",
        "order-amount" : 5000,
       }
    ]
}
```
#### cancel
```
{
            "data" : [
            
                {
                  delete(order);    
                    
                    
                }
            
            ]    
    
}
```



#### upaid
```
{
	"data" : [
		{
		"order_id" : 1,
		"price" : 500,
        cancel.delete(order);
       }
   ]
}
```

#### paying
```
		{
			"data" :[
	      {
		     "order_id" : 1,
		     "price" : 200,
		      cancel.delete(order);
         }
     ]
}
```

# Admin API
## stream
### stream-status
>GET /api/admin/v2/stream
##### Response:
```
{
	"code" : 0,
	"message" : "success",
	"data" : [
         {
		   "order_id" : 1,
		   "stream_id" : 1,
           "stream-status" : "streaming", 
		   "img" : "http://www.sss.com"
           "stream-address" : "xi'an" 
         }
    ]
}
```

### streamed
```
{
      "data" : [
      
              {
           return Confirmation-of-receipt;         
         }
    ]    
}
```

#### Confirmation-of-receipt
```
{
        "data" : [
            {
               payment.paying();
               order.delete(order);
        }
        
    ]    
    
}
```

## Payment
### Payment-List
>GET /api/admin/v1/payment
```
{
        "code" : 0 ,
        "message" : "success",
		"data" :[
	    { 
		   "type": "wechat",
		   "status" : "paid"
      }
   ]
}
```
