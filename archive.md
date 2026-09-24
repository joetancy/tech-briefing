---
layout: page
title: Archive
permalink: /archive/
---

{% for post in site.posts %}
- [{{ post.title }}]({{ post.url | relative_url }}) — {{ post.date | date: "%d %B %Y" }}
{% endfor %}
