---
layout: page
title: Musings
permalink: /musings/
---
{% for post in site.categories.musings %}
  <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
  <p>{{ post.date | date_to_string }}</p>
  <p>{{ post.excerpt }}</p>
  <hr>
{% endfor %}
