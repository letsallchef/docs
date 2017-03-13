---
title: Restaurants
cover: restaurants.jpg
endpoints: 
categories: api
layout: api    
---
Add, update and list restaurants.
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
| address | {} | Address details. |
| contact | {} | Contact details. |

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

## Search Restaurants	

## Get Restaurant

## Edit Restaurant

## Order Recipe

## Comment Restaurant

## Report Restaurant

## Delete Restaurant