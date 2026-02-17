---
layout: default
title: Musings
permalink: /musings/
---


### Recent musings, thoughts, and reflections on technology, innovation, and more.



{% for post in site.posts %}
  <div style="margin-bottom: 30px; padding-bottom: 20px; border-bottom: 1px solid #ddd;">
    <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
    <p style="color: #666; font-size: 0.9em;">{{ post.date | date: "%B %d, %Y" }}</p>
    {{ post.excerpt }}
    <a href="{{ post.url | relative_url }}">Read more →</a>
  </div>
{% endfor %}

{% if site.posts.size == 0 %}
  <p>No articles yet. Check back soon!</p>
{% endif %}
