---
layout: page
title: journal
permalink: /journal/
---


<ul>
  {% for post in site.categories.journal %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>