---
layout: page
title: posts
permalink: /posts/
description: News and updates
nav: false
order: 5
published: true
---

<div>






<ul class="post-list"> 

	

  {% for post in site.posts %}
    <li>
      <a href="{{ post.permalink }}">{{ post.title }}</a>
      <p>{{ post.excerpt }}</p>
    </li>
  {% endfor %}
</ul>
		 
		 

 
</div>
