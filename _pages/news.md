---
layout: page
title: news
permalink: /news/
description: News and updates
nav: false
order: 6
published: true
---

<div>






<ul class="post-list"> 

	
	{% assign news = site.news | reverse %}
    {% for item in news %}
	
		
		 
		 <li>
			<div class="row">
				<div class="col-sm-9">
					<h3> <a class="news-title" href="{{ item.url | prepend: site.baseurl }}">{{ item.date | date: "%b %-d, %Y" }}</a> </h3> 
					
					{% if item.inline %}
            {{ item.content | remove: '<p>' | remove: '</p>' | emojify }}
          {% else %}
            <a class="news-title" href="{{ item.url | prepend: site.baseurl }}">{{ item.title }}</a>
          {% endif %}
					
					</div>
					
					<div class="col-sm-3"> 
					
					{% if item.img %}
					<img class="card-img" src="{{ item.img }}" style="object-fit: cover; height: 90%" alt="image">
					{% endif %}
					 </div> 
					
					</div> 
		 </li> 
		 
		
		
		
    {% endfor %}
	
		
	
		 
		 
</ul>
 
</div>
