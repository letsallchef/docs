---
title: Groceries
cover: groceries.jpg
endpoints: 
categories: api
layout: api   
---
<!--more-->

## Add Grocery

`POST /groceries`

**Paramerts**

| Name | Type | Description |
| --- | --- | --- |
| title | String | Title of grocery. |
| description | String | Brief description of grocery. |
| also_known_as | String | Alternate name of grocery. |
| image | File | Image of grocery. |
| metric_units | [String] | Unit of grocery. |
| type | [String] | Type of grocery. |
| categories | [String] | Grocery categories. |

**Response**

{% highlight json %}
{
	"_id": ID
	"title": String
	"description": String
	"also_known_as": String
	"image": String
	"metric_units": [String]
	"type": [String]
	"categories": [String]
}
{% endhighlight %}


## Search Groceries

`GET /groceries`

**Parameters**

| Name | Type | Description |
| --- | --- | --- |
| title | String | Title of grocery. |
| type | [String] | Type of grocery. |
| categories | [String] | Grocery categories. |

**Response**

{% highlight json %}
[
	{
		"_id": ID
		"title": String
		"description": String
		"also_known_as": String
		"image": String
		"metric_units": [String]
		"type": [String]
		"categories": [String]
	}
]
{% endhighlight %}


## Get Grocery

`GET /groceries/:grocery_id`

**Response**

{% highlight json %}
{
	"_id": ID
	"title": String
	"description": String
	"also_known_as": String
	"image": String
	"metric_units": [String]
	"type": [String]
	"categories": [String]
}
{% endhighlight %}


## Edit Grocery

`PUT /groceries`

**Request**

| Name | Type | Description |
| --- | --- | --- |
| title | String | Title of grocery. |
| description | String | Brief description of grocery. |
| also_known_as | String | Alternate name of grocery. |
| image | File | Image of grocery. |
| metric_units | [String] | Unit of grocery. |
| type | [String] | Type of grocery. |
| categories | [String] | Grocery categories. |

**Response**

{% highlight json %}
{
	"_id": ID
	"title": String
	"description": String
	"also_known_as": String
	"image": String
	"metric_units": [String]
	"type": [String]
	"categories": [String]
}
{% endhighlight %}


## Add Grocery To Shopping List

`POST /groceries/:grocery_id/list`

**Response**

`Status 201`


## Remove Grocery From Shopping List

`DELETE /groceries/:grocery_id/unlist`

**Response**

`Status 204`


## Report Grocery

`POST /groceries/:grocery_id`

**Parameters**

| Name | Type | Description |
| --- | --- | --- |
| reason_type  | String | Type of the report reason. |
| reason_body  | String | Body of the report reason. |

**Response**

`Status 201`


## Delete Grocery

`DELETE /groceries/:grocery_id`

**Response**

`Status 204`