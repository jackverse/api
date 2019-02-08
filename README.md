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

> GET /api/user/v1/product/<productId>

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

#### Add-item-to-cart
```
{
            "data" : [
            
                        {
                        cart.add(product);        
                            
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

#### delete-product
```

{
            "data" : [
                  {
                      delete(product);            
                    
                }
            
        ]
}
```




#### select-count
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

#### settle-accounts
```
{
         "data" [
         
                        {
                           order.add(order);       
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



### upaid-order
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

### paying-order
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
```
{
              "data" : [
              
                     {
                         delete(order_id);      
            
            }        
              
            
        ]    
    
}

```

# Admin API


### order-management
>GET /api/admin/v2/order
```
{
           "code" : 0,
           "message" : "success",
           "data" : [
              {
               "oder_id" : 1,
               "account" : 5552,
               "product-name" : "MEIZU mobile",
               "description" : "blue",
               "payment-status" : "paying"

            } 
                
     ]
    
    
}

```
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
