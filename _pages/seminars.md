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
  collection: seminars
---



<!-- This loops through the paginated seminars -->
{% for seminar in paginator.seminars %}
  <ul class="seminar-list"> 
<li>
			<div class="row">
				<div class="col-sm-9">
					<h3> <a class="seminar-title" href="{{ seminar.url }}">{{ seminar.title }}</a> </h3> 
					<p class="author">
    <span class="date">{{ seminar.date | date: "%d %b %Y" }}</span>
  </p>
					{% if seminar.inline %}
            {{ seminar.content | remove: '<p>' | remove: '</p>' | emojify }}
          {% else %}
            
<a class="seminar-title" href="{{ seminar.url }}">{{ seminar.title }}</a>
         
 {% endif %}
					
					</div>
					
					<div class="col-sm-3"> 
					
					{% if seminar.img %}
					<img class="card-img" src="{{ seminar.img }}" style="object-fit: cover; height: 90%" alt="image">
					{% endif %}
					 </div> 
					
					</div> 
		 

</li> 	 
</ul>
{% endfor %}

<!-- Pagination links -->
<div class="Seminars page navigation">
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
