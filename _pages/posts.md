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
{% if paginator.total_pages > 1 %}
<div class="pagination">
  {% if paginator.previous_page %}
    <a href="{{ paginator.previous_page_path | relative_url }}">&laquo; Prev</a>
  {% else %}
    <span>&laquo; Prev</span>
  {% endif %}

  {% for page in (1..paginator.total_pages) %}
    {% if page == paginator.page %}
      <em>{{ page }}</em>
    {% elsif page == 1 %}
      <a href="{{ '/' | relative_url }}">{{ page }}</a>
    {% else %}
      <a href="{{ site.paginate_path | relative_url | replace: ':num', page }}">{{ page }}</a>
    {% endif %}
  {% endfor %}

  {% if paginator.next_page %}
    <a href="{{ paginator.next_page_path | relative_url }}">Next &raquo;</a>
  {% else %}
    <span>Next &raquo;</span>
  {% endif %}
</div>
{% endif %}




