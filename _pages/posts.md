---
layout: page
title: news
permalink: /posts/
description: News and updates
nav: true
order: 5
published: true
pagination:
  enabled: true
---



<!-- This loops through the paginated posts -->
{% for post in paginator.posts %}
  <ul class="post-list"> 
<li>
			<div class="row">
				<div class="col-sm-9">
					<h3> <a class="news-title" href="{{ post.url }}">{{ post.title }}</a> </h3> 
					<p class="author">
    <span class="date">{{ post.date | date: "%d %b %Y" }}</span>
  </p>
					{% if post.inline %}
            {{ post.content | remove: '<p>' | remove: '</p>' | emojify }}
          {% else %}
            
<a class="news-title" href="{{ post.url }}">{{ post.title }}</a>
         
 {% endif %}
					
					</div>
					
					<div class="col-sm-3"> 
					
					{% if post.img %}
					<img class="card-img" src="{{ post.img }}" style="object-fit: cover; height: 90%" alt="image">
					{% endif %}
					 </div> 
					
					</div> 
		 

</li> 	 
</ul>
{% endfor %}

<!-- Pagination links -->
<div class="Blog page navigation">
  {% if paginator.previous_page %}
    <a href="{{ paginator.previous_page_path }}" class="previous">
      Previous
    </a>
  {% else %}
    <span class="previous page-item disabled">Previous </span>
  {% endif %}
  <span class="page_number ">
   {{ paginator.page }} of {{ paginator.total_pages }}
  </span>
  {% if paginator.next_page %}
    <a href="{{ paginator.next_page_path }}" class="next">Next</a>
  {% else %}
    <span class="next page-item disabled">Next</span>
  {% endif %}
</div>


