---
layout: page
title: Fyzika
permalink: /fyzika/
---

{% for post in site.posts %}
  {% if post.categories contains 'Fyzika' %}
    
[{{post.title}}]({{post.url}})<br/><small>{{ post.date | date_to_long_string }}</small>
    
  {% endif %}
{% endfor %}
