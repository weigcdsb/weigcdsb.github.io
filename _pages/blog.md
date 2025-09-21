---
layout: blog
title: Blog
permalink: /blog/
nav: true
# pagination:
#   enabled: true
#   per_page: 10
#   sort_reverse: true
---

<h2>Posts ({{ site.posts | size }})</h2>
<ul>
{% for post in site.posts %}
  <li><a href="{{ post.url | relative_url }}">{{ post.title }}</a> — {{ post.date | date: "%Y-%m-%d" }}</li>
{% endfor %}
</ul>