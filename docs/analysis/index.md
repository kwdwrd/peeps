---
layout: default
title: Analysis
permalink: /analysis/
description: Synthesis and data-backed takes that connect research threads.
---

<div class="section-card" markdown="1">
# Analysis

Cross-cutting syntheses that weave together multiple studies and data.

{% assign analysis_posts = site.analysis | sort: "date" | reverse %}
{% for post in analysis_posts %}
- [{{ post.title }}]({{ site.baseurl }}{{ post.url }})
  <span style="color:#6b7280; font-size:0.9rem;"> — {{ post.date | date: "%b %-d, %Y" }}</span>
  <div style="color:#4b5563; margin: 0.2rem 0 0.8rem 1rem;">{{ post.summary | default: post.excerpt | strip_html | truncate: 180 }}</div>
{% endfor %}
</div>
