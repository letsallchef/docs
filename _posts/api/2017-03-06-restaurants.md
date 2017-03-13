---
title: Restaurants
cover: restaurants.jpg
endpoints: 9
categories: api
layout: api    
---
Know about the menus, reviews and rating of the restaurants nearby. 
<!--more-->

## Add Restaurant

`POST /restaurants`

**Parameters**

| Name | Type | Description |
| --- | --- | --- |
| title | String | Name of the restaurant. |
| logo | String | Logo of the restaurant |
| cover | file | Cover image of the restaurant. |
| url | String | User friendly URL of the restaurant. |
| type | [String] | Type of the restaurant. |
| categories | [String] | Categories of the restaurant. |
| accepts_reservations | String | Whether the restaurant accepts reservations. |
| serves_cuisine | [String] | List of cuisines served. |
| star_rating | String | Star rating of the restaurant. |
| opening_hours | [String] | Opening Hours. |
| payment_methods | [String] | List of payment methods accepted. |
| can_home_deliver | Boolean | Whether home delivers food. |
| price_range | [String] | Price range of items. |
| photos | [file] | List of photos. |
| address | { } | Address details. |
| contact | { } | Contact details. |

**Response**

{% highlight json %}
{
	"_id": ID,
	"title": String,
	"logo": String,
	"url": String,
	"type": [String],
	"categories": [String],
	"accepts_reservations": String,
	"serves_cuisine": [String],
	"star_rating": String,
	"opening_hours": [String],
	"payment_methods": [String],
	"can_home_delever": Boolean,
	"price_range": [String],
	"photos": [String],
	"address": {       
	    "addressLine1": String,
	    "addressLine2": String,
	    "landmark": String,
	    "state": String,
	    "city": String,
	    "district": String,
	    "country": String,
	    "geo": {
	        "latitude": Number,
	        "longitude": Number
	    }
	},
	"contact": {
	    "email": String,
	    "phone": String
	},
	"owner": {
	    "user_id": ID,
	    "user_avatar": String,
	    "user_username": String,
	    "user_first_name": String,
	    "user_rating": Number
	}
}
{% endhighlight %}


## Search Restaurants

`GET /restaurants`

**Response**

{% highlight json %}
[
	{
		"_id": ID,
		"title": String,
		"url": String,
		"opening_hours": [String],
		"can_home_delever": Boolean,
		"address": {
		    "addressLine1": String,
		    "addressLine2": String,
		    "landmark": String,
		    "state": String,
		    "city": String,
		    "district": String,
		    "country": String,
		    "geo": {
		        "latitude": Number,
		        "longitude": Number
		    }
		},
		"contact": {
		    "email": String,
		    "phone": String
		}
	}
]
{% endhighlight %}


## Get Restaurant

`GET /restaurants/:restaurant_id`

**Response**

{% highlight json %}
{
	"_id": ID,
	"title": String,
	"logo": String,
	"url": String,
	"type": [String],
	"categories": [String],
	"accepts_reservations": String,
	"serves_cuisine": [String],
	"star_rating": String,
	"opening_hours": [String],
	"payment_methods": [String],
	"can_home_delever": Boolean,
	"price_range": [String],
	"photos": [String],
	"address": {       
	    "addressLine1": String,
	    "addressLine2": String,
	    "landmark": String,
	    "state": String,
	    "city": String,
	    "district": String,
	    "country": String,
	    "geo": {
	        "latitude": Number,
	        "longitude": Number
	    }
	},
	"contact": {
	    "email": String,
	    "phone": String
	},
	"owner": {
	    "user_id": ID,
	    "user_avatar": String,
	    "user_username": String,
	    "user_first_name": String,
	    "user_rating": Number
	},
	"comments": {
	    "user_id": ID,
	    "user_avatar": String,
	    "user_username": String,
	    "user_first_name": String,
	    "user_rating": Number,
	    "comment": String,
	    "rating": Number
	}
}
{% endhighlight %}


## Edit Restaurant

`POST /restaurants`

**Parameters**

| Name | Type | Description |
| --- | --- | --- |
| title | String | Name of the restaurant. |
| logo | String | Logo of the restaurant |
| cover | file | Cover image of the restaurant. |
| url | String | User friendly URL of the restaurant. |
| type | [String] | Type of the restaurant. |
| categories | [String] | Categories of the restaurant. |
| accepts_reservations | String | Whether the restaurant accepts reservations. |
| serves_cuisine | [String] | List of cuisines served. |
| star_rating | String | Star rating of the restaurant. |
| opening_hours | [String] | Opening Hours. |
| payment_methods | [String] | List of payment methods accepted. |
| can_home_deliver | Boolean | Whether home delivers food. |
| price_range | [String] | Price range of items. |
| photos | [file] | List of photos. |
| address | { } | Address details. |
| contact | { } | Contact details. |

**Response**

{% highlight json %}
{
	"_id": ID,
	"title": String,
	"logo": String,
	"url": String,
	"type": [String],
	"categories": [String],
	"accepts_reservations": String,
	"serves_cuisine": [String],
	"star_rating": String,
	"opening_hours": [String],
	"payment_methods": [String],
	"can_home_delever": Boolean,
	"price_range": [String],
	"photos": [String],
	"address": {       
	    "addressLine1": String,
	    "addressLine2": String,
	    "landmark": String,
	    "state": String,
	    "city": String,
	    "district": String,
	    "country": String,
	    "geo": {
	        "latitude": Number,
	        "longitude": Number
	    }
	},
	"contact": {
	    "email": String,
	    "phone": String
	},
	"owner": {
	    "user_id": ID,
	    "user_avatar": String,
	    "user_username": String,
	    "user_first_name": String,
	    "user_rating": Number
	}
}
{% endhighlight %}

## Order Recipe

## Order Grocery

`POST /restaurants/order`

**Parameters**

| Name | Type | Description |
| --- | --- | --- |
| item_id | ID | ID of the store grocery. |
| quantity | Number | Quantity of the store grocery. |

**Response**

`Status: 201`


## Comment Restaurant

`PUT /restaurants/:store_id`

**Parameters**

| Name | Type | Description |
| --- | --- | --- |
| comment  | String | Body of the comment. |
| rating | Number | Rating of the recipe in the order of 1-5 |

**Response**

`Status: 201`


## Report Restaurant

`POST /restaurants/:store_id`

**Parameters**

| Name | Type | Description |
| --- | --- | --- |
| reason_type  | String | Type of the report reason. |
| reason_body  | String | Body of the report reason. |

**Response**

`Status: 201`


## Delete Restaurant

`DELETE /restaurants/:store_id`

**Response**

`Status: 204`