---
layout: default
title: About
permalink: /about/
team: [alex, priya, morgan]
---

<div class="section-card" markdown="1">
# About

We dig into emerging research, connect evidence across domains, and publish data-backed syntheses. Below are the people behind the work.
</div>

<div class="author-grid">
  {% for member_id in page.team %}
    {% assign member = site.data.authors[member_id] %}
    {% if member %}
      <div class="author-card">
        <div class="author-avatar">
          {% if member.image %}
            <img src="{{ site.baseurl }}{{ member.image }}" alt="{{ member.name }}" loading="lazy" />
          {% else %}
            <div class="author-placeholder">{{ member.name | slice: 0,1 }}</div>
          {% endif %}
        </div>
        <div class="author-details">
          <div class="author-name">{{ member.name }}</div>
          <div class="author-bio">{{ member.bio }}</div>
        </div>
      </div>
    {% endif %}
  {% endfor %}
</div>
