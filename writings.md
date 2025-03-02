---
layout: page
title: Writings
permalink: /writings/
---
{% for post in site.categories.writings %}
  <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
  <p>{{ post.date | date_to_string }}</p>
  <p>{{ post.excerpt }}</p>
  <hr>
{% endfor %}
