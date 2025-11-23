---
layout: default
title: Blog
permalink: /blog/
---

<div class="section-card">
# Blog

{% for post in site.posts %}
- [{{ post.title }}]({{ site.baseurl }}{{ post.url }})
  <span style="color:#6b7280; font-size:0.9rem;">
    — {{ post.date | date: "%b %-d, %Y" }}
  </span>
{% endfor %}
</div>

