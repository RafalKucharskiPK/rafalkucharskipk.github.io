---
layout: page
title: news
permalink: /news/
description: News and updates
nav: true
order: 5
published: true

---

<div>






<ul class="post-list"> 
	
	
	
	{% assign news = site.news | reverse %}
    {% for item in paginator.posts %}
	
		
		 
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
					
					<div class="col-sm-3"> <img class="card-img" src="/al-folio/assets/img/9.jpg" style="object-fit: cover; height: 90%" alt="image"> </div> 
					
					</div> 
		 </li> 
		 
		
		
		
    {% endfor %}
	
		
	
		 
		 
</ul>
 
</div>
<!-- Pagination links -->
<div class="pagination">
  {% if paginator.previous_page %}
    <a href="{{ paginator.previous_page_path }}" class="previous">
      Previous
    </a>
  {% else %}
    <span class="previous">Previous</span>
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
