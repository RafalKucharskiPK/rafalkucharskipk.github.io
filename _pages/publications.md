---
layout: page
permalink: /papers/
title: papers
description: journal papers and arXiv preprints in reversed chronological order.
years: [2023, 2022, 2021, 2020, 2019, 2017]
nav: true
order: 5
published: true
---

<div class="publications">

{% for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}

</div>
