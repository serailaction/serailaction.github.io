---
layout: page
title: Southeastern Railway Action Group
tagline: 
---
{% include JB/setup %}
 
<div class="container" id="indexpage">
	<div class="col-md-9" id="indexpage">
	{% for post in site.posts %}
    {% capture display %}{{post.indexhide}}{% endcapture %}
    {% if display != 'true' %}
    {% capture stickyX %}{{post.categories}}{% endcapture %}
    {% if stickyX == "pinned post" %}
    <span><a href="{{ BASE_PATH }}{{ post.url }}"  style="text-decoration: none"><h1>{{ post.title }}</h1></a></span><br>
                    <div class="highlighter">pinned post</div>
                    <b>{{ post.date | date_to_string }}</b>
                    {% if post.author %}
                        | {{post.author}}
                    {% endif %}
					<br>                       
                       {{post.content | split:"SPLIT_HERE" | first}}

                        {% capture posted_text %} {{post.content | split:"SPLIT_HERE" | first}}{% endcapture %}
                        {% assign postCountX = posted_text | number_of_words %}
                        {% assign origCountX = post.content | number_of_words %}
                        {% assign postCount = postCountX | times: 1 %}
                        {% assign origCount = origCountX | times: 1 %}
                        {% if postCount < origCount %}
                        <b><a href="{{ BASE_PATH }}{{ post.url }}"  style="text-decoration: none">[more]</a></b>
                      
                         
                        {% else %}
                        </a>   
                        
                        {% endif %}
      
                        </p></blockquote>
                        </li></ul></blockquote>
                        
                        <!--
					<br><a href="https://twitter.com/share" class="twitter-share-button" data-url="http://philrogers.me{{ BASE_PATH }}{{ post.url }}" data-via="philmonkey">Tweet</a>
                    -->
                    <br>
     {% endif %} 
     {% endif %}
	{% endfor %}	

    {% for post in site.posts %}
    {% capture display %}{{post.indexhide}}{% endcapture %}
    {% if display != 'true' %}
    {% capture stickyX %}{{post.categories}}{% endcapture %}
{% if stickyX != "pinned post" %}
    <span><a href="{{ BASE_PATH }}{{ post.url }}"  style="text-decoration: none"><h1>{{ post.title }}</h1></a></span><br>
    {% if stickyX != '' %}
                    <div class="highlighter">{{stickyX}}</div>
                    
                    {% endif %}
					<b>{{ post.date | date_to_string }}</b>
					                    {% if post.author %}
                        | {{post.author}}
                    {% endif %}
					
					<br>
                
                      
                        {{post.content | split:"SPLIT_HERE" | first}}

                        {% capture posted_text %} {{post.content | split:"SPLIT_HERE" | first}}{% endcapture %}
                        {% assign postCountX = posted_text | number_of_words %}
                        {% assign origCountX = post.content | number_of_words %}
                        {% assign postCount = postCountX | times: 1 %}
                        {% assign origCount = origCountX | times: 1 %}
                        {% if postCount < origCount %}
                        <b><a href="{{ BASE_PATH }}{{ post.url }}"  style="text-decoration: none">[more]</a></b>
                      
                         
                        {% else %}
                        </a>   
                        
                        {% endif %}
                    
                        </p></blockquote>
                        </li></ul></blockquote>
                        
                        <!--
					<br><a href="https://twitter.com/share" class="twitter-share-button" data-url="http://philrogers.me{{ BASE_PATH }}{{ post.url }}" data-via="philmonkey">Tweet</a>
                    -->
                    <br>
                    
      {% endif %}
      {% endif %}
	{% endfor %}	    

</div>
<div class="col-md-3">
</div>
</div>


        
