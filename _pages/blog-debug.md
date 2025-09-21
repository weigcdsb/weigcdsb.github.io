---
layout: blog
title: Blog-debug
permalink: /blog-debug/
nav: true
---

<h2>Posts ({{ site.posts | size }})</h2>
<ul>
{% for post in site.posts %}
  <li><a href="{{ post.url | relative_url }}">{{ post.title }}</a> — {{ post.date | date: "%Y-%m-%d" }}</li>
{% endfor %}
</ul>
