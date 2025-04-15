---
layout: page
title: people
permalink: /group/
description: Meet Rafał Kucharski and his dynamic research group at Jagiellonian University in Kraków. From Principal Investigators to students, this team engages in groundbreaking projects on transport systems, machine learning, and urban mobility. Discover their members, achievements, and ongoing contributions to advancing these fields.
nav: true
order: 2
published: true
display_categories: [PI, PostDocs, PhD students, students, former, others]
horizontal: false
---


<center><img src="{{ site.baseurl }}/assets/img/team.jpg" width="600" height="400"></center>


<div class="projects">
  {% if site.enable_project_categories and page.display_categories %}
  <!-- Display categorized projects -->
    {% for category in page.display_categories %}
      <h2 class="category">{{ category }}</h2>
      {% assign categorized_projects = site.research | where: "category", category %}
      {% assign sorted_projects = categorized_projects | sort: "author" %}
      <!-- Generate cards for each project -->
      {% if page.horizontal %}
        <div class="container">
          <div class="row row-cols-2">
          {% for project in sorted_projects %}
            {% include projects_horizontal.html %}
          {% endfor %}
          </div>
        </div>
      {% else %}
        <div class="_grid">
          {% for project in sorted_projects %}
            {% include projects.html %}
          {% endfor %}
        </div>
      {% endif %}
    {% endfor %}

  {% else %}
  <!-- Display projects without categories -->
    {% assign sorted_projects = site.research | sort: "author" %}
    <!-- Generate cards for each project -->
    {% if page.horizontal %}
      <div class="container">
        <div class="row row-cols-2">
        {% for project in sorted_projects %}
          {% include projects_horizontal.html %}
        {% endfor %}
        </div>
      </div>
    {% else %}
      <div class="_grid">
        {% for project in sorted_projects %}
          {% include projects.html %}
        {% endfor %}
      </div>
    {% endif %}

  {% endif %}
