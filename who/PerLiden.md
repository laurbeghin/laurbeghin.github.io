---
layout: default
title: who
permalink: /BioPerLiden 
---

<h4>Per Liden</h4>

<div>I’m Per Lidén, software engineer and part of the team developing OpenJDK at Oracle. I’m lead for the <a href="https://wiki.openjdk.java.net/display/zgc/Main">ZGC</a> project, where we’re developing the next generation low-latency garbage collector for Java. The views expressed on this blog are my own and do not necessarily reflect the views of my employer.</div>

<h4>Posts</h4>

  <ul>	  
  {% for post in site.posts %}
  {% if post.author == "Per Liden" %}
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

<h4>Videos</h4>
<center>

<iframe width="560" height="315" src="https://www.youtube.com/embed/7k_XfLGu-Ts" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
<div class="date">The Z Garbage Collector (ZGC) - Overview (Oct. 2018)</div><br/>

<iframe width="560" height="315" src="https://www.youtube.com/embed/kF_r3GE3zOo" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
<div class="date">ZGC: A Scalable Low-Latency Garbage Collector (Oct. 2018)</div>

</center>
