---
layout: page
title: Blog debug
permalink: /blog-debug/
nav: false
---
Total posts seen by Jekyll: {{ site.posts | size }}
<ul>
{% for p in site.posts %}
<li><a href="{{ p.url | relative_url }}">{{ p.title }}</a> — {{ p.date | date: "%F" }}</li>
{% endfor %}
</ul>
