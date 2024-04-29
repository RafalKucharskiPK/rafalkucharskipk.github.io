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
<nav aria-label="Blog page naviation">
<ul class="pagination pagination-lg justify-content-center">
  {% if paginator.previous_page %}
  
  
 <li class="page-item disabled"> <a class="page-link" href="{{ paginator.previous_page_path | relative_url }}" tabindex="-1" aria-disabled="">Newer</a> </li>
  {% else %}
   <li class="page-item disabled"> <a class="page-link" href="{{ paginator.previous_page_path | relative_url }}" tabindex="-1" aria-disabled="">Newer</a> </li>
  {% endif %}

  {% for page in (1..paginator.total_pages) %}
    {% if page == paginator.page %}
       <li class="page-item active"> <a class="page-link" href="{{ page }}" title="blog">{{ page }}</a> </li>
    {% elsif page == 1 %}
     <li class="page-item "> <a class="page-link" href="{{ '/' | relative_url }}" title="blog - page {{ page }}">{{ page }}</a> </li>
    {% else %}
      <li class="page-item "> <a class="page-link" href="{{ site.paginate_path | relative_url | replace: ':num', page }}" title="blog - page {{ page }}">{{ page }}</a> </li>
     
    {% endif %}
  {% endfor %}

  {% if paginator.next_page %}
    <li class="page-item "> <a class="page-link" href="{ paginator.next_page_path | relative_url }}">Older</a> </li>
   
  {% else %}
    <span>Next</span>
  {% endif %}
  </ul>
      </nav>
{% endif %}
