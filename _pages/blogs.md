---
layout: page
title: Blogs
permalink: /blogs/
nav: true
---

<!-- <h2>Posts ({{ site.posts | size }})</h2> -->
{% assign current_year = "" %}
{% for post in site.posts %}
  {% assign y = post.date | date: "%Y" %}
  {% if y != current_year %}
    {% unless forloop.first %}</ul>{% endunless %}
## **{{ y }}**
    <ul>
    {% assign current_year = y %}
  {% endif %}
  <li><a href="{{ post.url | relative_url }}">{{ post.title }}</a> — {{ post.date | date: "%Y-%m-%d" }}</li>
{% endfor %}
{% if current_year != "" %}</ul>{% endif %}


<!-- <ul>
{% for post in site.posts %}
  <li><a href="{{ post.url | relative_url }}">{{ post.title }}</a> — {{ post.date | date: "%Y-%m-%d" }}</li>
{% endfor %}
</ul> -->
