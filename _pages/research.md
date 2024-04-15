---
layout: page
title: research
permalink: /research/
description: Basic info and references to our grants, significant current and past research and finally ride-pooling our main current stream of research.
nav: true
order: 4
display_categories: [grants, varia, pooling]
horizontal: false
published: false
---

<div class="projects">
  {% if site.enable_project_categories and page.display_categories %}
  <!-- Display categorized projects -->
    {% for category in page.display_categories %}
      <h2 class="category">{{ category }}</h2>
      {% assign categorized_projects = site.research | where: "category", category %}
      {% assign sorted_projects = categorized_projects | sort: "importance" %}
      <!-- Generate cards for each project -->
      {% if page.horizontal %}
        <div class="container">
          <div class="row row-cols-2">
          {% for project in sorted_projects %}
            {% include research.html %}
          {% endfor %}
          </div>
        </div>
      {% else %}
       <div class="d-flex align-content-stretch justify-content-center flex-wrap no-gutters mx-n2">

          {% for project in sorted_projects %}
            {% include research.html %}
          {% endfor %}
        </div>
      {% endif %}
    {% endfor %}

  {% else %}
  <!-- Display projects without categories -->
    {% assign sorted_projects = site.research | sort: "importance" %}
    <!-- Generate cards for each project -->
    {% if page.horizontal %}
      <div class="container">
        <div class="row row-cols-2">
        {% for project in sorted_projects %}
          {% include research.html %}
        {% endfor %}
        </div>
      </div>
    {% else %}
      <div class="d-flex align-content-stretch justify-content-center flex-wrap no-gutters mx-n2">
        {% for project in sorted_projects %}
          {% include research.html %}
        {% endfor %}
      </div>
    {% endif %}

  {% endif %}


