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


## List Groceries

## Search Groceries

## Get Grocery

## Edit Grocery

## Add Grocery To Shopping List

## Report Grocery

## Delete Grocery