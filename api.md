---
title: "API Documentation"
layout: default
permalink: /api-documentation
---
<br>
<div class="ui container">
	<header class="ui grey center aligned segment">
		<h1 class=" header">API Documentation</h1>
	</header>
</div>
<br>
<div class="ui stackable container grid">
	{% for api in site.categories.api %}
	<div class="four wide column">
		<div class="ui card">
			<div class="image">
				<img src="{{ site.baseurl }}/uploads/posts/api/{{ api.cover }}">
			</div>
			<div class="content">
				<a href="{{ site.baseurl }}{{ api.url }}" class="header">{{ api.title }}</a>
				<div class="description">
					{{ api.brief }}
				</div>
			</div>
			<div class="extra content">
				<a>
					<i class="life ring icon"></i>
					{{ api.endpoints }} Endpoints
				</a>
			</div>
		</div>
	</div>
	{% endfor %}
</div>