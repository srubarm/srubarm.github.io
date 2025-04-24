---
layout: page
title: Astronomie
permalink: /astronomie/
---

{% for post in site.posts %}
  {% if post.categories contains 'Astronomie' %}
    
[{{post.title}}]({{post.url}})<br/><small>{{ post.date | date_to_long_string }}</small>
    
  {% endif %}
{% endfor %}
