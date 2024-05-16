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
<div class="pagination">
  {% if paginator.previous_page %}
    <a href="{{ paginator.previous_page_path }}" class="previous">
      Previous 
    </a>
  {% else %}
    <span class="previous">Previous </span>
  {% endif %}
  <span class="page_number ">
    Page: {{ paginator.page }} of {{ paginator.total_pages }}
  </span>
  {% if paginator.next_page %}
    <a href="{{ paginator.next_page_path }}" class="next">Next</a>
  {% else %}
    <span class="next ">Next</span>
  {% endif %}
</div>


<nav aria-label="Blog page navigation"> <ul class="pagination pagination-lg justify-content-center"> <li class="page-item disabled"> <a class="page-link" href="" tabindex="-1" aria-disabled="">Newer</a> </li> <li class="page-item active"> <a class="page-link" href="/al-folio/blog/index.html" title="blog">1</a> </li> <li class="page-item "> <a class="page-link" href="/al-folio/blog/page/2/index.html" title="blog - page 2">2</a> </li> <li class="page-item "> <a class="page-link" href="/al-folio/blog/page/3/index.html" title="blog - page 3">3</a> </li> <li class="page-item "> <a class="page-link" href="/al-folio/blog/page/4/index.html" title="blog - page 4">4</a> </li> <li class="page-item "> <a class="page-link" href="/al-folio/blog/page/5/index.html" title="blog - page 5">5</a> </li> <li class="page-item "> <a class="page-link" href="/al-folio/blog/page/2/">Older</a> </li> </ul> </nav>
