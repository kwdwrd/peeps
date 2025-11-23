---
layout: default
title: Home
---

<div class="section-card" markdown="1">
# Welcome

This is my modern site hosted on GitHub Pages.

- Read the latest posts on the [blog]({{ site.baseurl }}/blog/).
- Explore datasets in the [data repository]({{ site.baseurl }}/data/).
- Learn more [about me]({{ site.baseurl }}/about/).
</div>

<div class="section-card">
## Recent Posts

<ul>
  {% for post in site.posts limit:5 %}
    <li>
      <a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a>
      <span style="color:#6b7280; font-size:0.9rem;">
        — {{ post.date | date: "%b %-d, %Y" }}
      </span>
    </li>
  {% endfor %}
</ul>
</div>

