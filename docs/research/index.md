---
layout: default
title: Research
permalink: /research/
description: Summaries of recent papers, articles, and reports.
---

<div class="section-card" markdown="1">
# Research

Short takes on recent papers, articles, and reports.

{% assign research_posts = site.research | sort: "date" | reverse %}
{% for post in research_posts %}
- [{{ post.title }}]({{ site.baseurl }}{{ post.url }})
  <span style="color:#6b7280; font-size:0.9rem;"> — {{ post.date | date: "%b %-d, %Y" }}</span>
  <div style="color:#4b5563; margin: 0.2rem 0 0.8rem 1rem;">{{ post.summary | default: post.excerpt | strip_html | truncate: 180 }}</div>
{% endfor %}
</div>
