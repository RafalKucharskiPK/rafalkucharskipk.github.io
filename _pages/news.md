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
    <table>
    {% assign news = site.news | reverse %}
    {% for item in news %}
      <tr>
        <th class="date">{{ item.date | date: "%b %-d, %Y" }}</th>
        <td class="announcement">
          {% if item.inline %}
            {{ item.content | remove: '<p>' | remove: '</p>' | emojify }}
          {% else %}
            <a class="news-title" href="{{ item.url | prepend: site.baseurl }}">{{ item.title }}</a>
          {% endif %}
        </td>
      </tr>
    {% endfor %}
    </table>
</div>
