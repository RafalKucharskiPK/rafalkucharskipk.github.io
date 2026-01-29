---
layout: page
permalink: /papers/
title: papers
description: Explore journal papers and arXiv preprints by Rafał Kucharski and his research group at Jagiellonian University, presented in reversed chronological order. Delve into studies on transportation systems, machine learning, and urban mobility, showcasing groundbreaking insights and academic achievements.
years: [2026, 2025, 2024, 2023, 2022, 2021, 2020]
nav: true
order: 4
published: true
---

<div class="publications">

{% for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers -q @*[year={{y}} && project~= /(SUMO|OPUS|COeXISTENCE)/] %}
{% endfor %}

</div>
