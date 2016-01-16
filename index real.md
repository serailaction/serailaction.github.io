---
layout: page
title: Phil Rogers
tagline: thoughts, ideas, random stuff...
---
{% include JB/setup %}



## todo stuff

Read [Jekyll Quick Start](http://jekyllbootstrap.com/usage/jekyll-quick-start.html)

Complete usage and documentation available at: [Jekyll Bootstrap](http://jekyllbootstrap.com)



    
## Recent posts

Recent posts can be found here.

All posts can be found in the Archive!

<div class="posts">
	{% for post in site.posts %}
		<span><a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></span> {{ post.date | date_to_string }}
		<br>
		{{ post.summary }}
		<br><br>
	{% endfor %}
</div>


## Stuff

I could write more stuff if I wanted to here