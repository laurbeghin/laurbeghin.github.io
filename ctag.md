---
layout: default
title: tag
permalink: /tag
---
{% assign sortedtags = site.tags | sort %}

{% assign author = site.authors | where:"short_name", post.author %}

{% for tag in sortedtags %}
  <h3 id="{{ tag[0] | downcase }}">{{ tag[0] }}</h3>
  <ul>	  
    {% for post in tag[1] %}
	{% capture url_to_use %}{{ post.url }}{% endcapture %}
	{% if post.redirect_url %}
        	{% capture url_to_use %}{{ post.redirect_url }}{% endcapture %}
	{% endif %}
	<li>
		<a href="{{ site.baseurl }} {{ url_to_use }}">{{ post.title }}</a>
		<span id="post-info">(<a href="{{ author[0].url }}">{{ author[0].name }}</a> on {{ post.date | date: "%B %e, %Y" }})</span>
	</li>
    {% endfor %}
  </ul>
{% endfor %}
