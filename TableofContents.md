---
layout: page
title: Contents
permalink: /tableofcontents/
---

<div>
  <p><i>Hover over the title link to preview the blog post<br>The square brackets to the right of the title is the last update time.</i></p>
</div>

<ul>
  {% for post in site.posts %}
    <li>
      {{ post.date | date: '%Y-%m-%d'}}
      <a href="{{ post.url }}" title="{{ post.excerpt | remove: '<p>' | remove: '</p>' }}">{{ post.title }}</a>
      {% if post.update %}
          [{{ post.update }}]
      {% endif %}
    </li>
  {% endfor %}
</ul>
