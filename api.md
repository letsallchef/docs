---
layout: api
title: "API Documentation"
---
<div class="ui stackable grid container">
	{% for api in site.categories.api %}
	<div class="four wide column">
		<div class="ui card">
			<div class="image">
				<img src="{{ site.baseurl }}/uploads/posts/{{ api.cover }}">
			</div>
			<div class="content">
				<a href="{{ api.url }}" class="header">{{ api.title }}</a>
				<div class="meta">
					<span class="date">Last Updated : {{ api.date | date_to_long_string }}</span>
				</div>
				<div class="description">
					{{ api.excerpt }}
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