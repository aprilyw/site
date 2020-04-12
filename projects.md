---
layout: page
title: projects
permalink: /projects/
---


<ul>
  {% for post in site.categories.projects %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>