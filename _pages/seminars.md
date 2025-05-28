---
layout: page
title: seminars
permalink: /seminars/
description: Rafał Kucharski and his research group at Jagiellonian University from the inside. Stay up to date with the latest achievements, meet researchers we are working with. 
nav: true
order: 6
published: true
pagination:
  enabled: true
---



<!-- This loops through the paginated seminars -->
{% for seminars in paginator.seminars %}
  <ul class="seminars-list"> 
<li>
			<div class="row">
				<div class="col-sm-9">
					<h3> <a class="seminars-title" href="{{ seminars.url }}">{{ seminars.title }}</a> </h3> 
					<p class="author">
    <span class="date">{{ seminars.date | date: "%d %b %Y" }}</span>
  </p>
					{% if seminars.inline %}
            {{ seminars.content | remove: '<p>' | remove: '</p>' | emojify }}
          {% else %}
            
<a class="seminars-title" href="{{ seminars.url }}">{{ seminars.title }}</a>
         
 {% endif %}
					
					</div>
					
					<div class="col-sm-3"> 
					
					{% if seminars.img %}
					<img class="card-img" src="{{ seminars.img }}" style="object-fit: cover; height: 90%" alt="image">
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
