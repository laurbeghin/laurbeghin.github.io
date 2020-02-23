---
layout: default
title: who
permalink: /BioJornVernee
---

<h4>Jorn Vernee</h4>

<div>Jorn Vernee bio... Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</div>


  <ul>	  
  {% for post in site.posts %}
  {% if post.author == "Jorn Vernee" %} 
	{% capture url_to_use %}{{ post.url" }}{% endcapture %}
        {% if post.redirect_url %}
           {% capture url_to_use %}{{ post.redirect_url" }}{% endcapture %}
        {% endif %}
	<li><a href="{{ site.baseurl }} {{ url_to_use }}">{{ post.title }}
	    <div class="date">{{ post.date | date: "%B %e, %Y" }}</div></a>
	</li>
  {% endif %}
  {% endfor %}
  </ul>
