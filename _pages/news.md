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
    {% for item in news %}
	
		
		 
		 <li>
			<div class="row">
				<div class="col-sm-9">
					<h3> <a class="news-title" href="{{ item.url | prepend: site.baseurl }}">{{ item.title }}</a> </h3> 
					
					<p>this is what advanced image components could look like</p> 
					<p class="post-meta">{{ item.date | date: "%b %-d, %Y" }}</p> <p class="post-tags"> <a href="/al-folio/blog/2024"> <i class="fa-solid fa-calendar fa-sm"></i> 2024 </a> &nbsp; · &nbsp; <a href="/al-folio/blog/tag/formatting"> <i class="fa-solid fa-hashtag fa-sm"></i> formatting</a> &nbsp; <a href="/al-folio/blog/tag/images"> <i class="fa-solid fa-hashtag fa-sm"></i> images</a> &nbsp; &nbsp; · &nbsp; <a href="/al-folio/blog/category/sample-posts"> <i class="fa-solid fa-tag fa-sm"></i> sample-posts</a> &nbsp; </p>
					
					</div>
					
					<div class="col-sm-3"> <img class="card-img" src="/al-folio/assets/img/9.jpg" style="object-fit: cover; height: 90%" alt="image"> </div> 
					
					</div> 
		 </li> 
		 
		
		
		
    {% endfor %}
	
		
	
		 
		 
</ul>
 
</div>
