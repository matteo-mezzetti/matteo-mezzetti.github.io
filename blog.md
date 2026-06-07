---
layout: default
title: Blog
---

<div class="page-header">
  <h1>Writing</h1>
  <p>Things I'm learning, building, and breaking.</p>
</div>

<div class="section">
  {% for post in site.posts %}
  <div class="item-row">
    <a href="{{ post.url | relative_url }}" class="item-link">{{ post.title }} →</a>
    <p class="item-desc">{{ post.excerpt | strip_html | truncatewords: 20 }}</p>
  </div>
  {% endfor %}
  {% if site.posts.size == 0 %}
  <div class="item-row">
    <p class="item-desc">No posts yet — check back soon.</p>
  </div>
  {% endif %}
</div>
