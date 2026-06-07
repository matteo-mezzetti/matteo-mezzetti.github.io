---
layout: default
title: Blog
---

# Blog

Things I'm learning, building, and breaking.

<ul class="post-list">
  {% for post in site.posts %}
  <li>
    <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    <span class="post-date">{{ post.date | date: "%b %-d, %Y" }}</span>
  </li>
  {% endfor %}
  {% if site.posts.size == 0 %}
  <li style="border: none; color: var(--muted); font-style: italic;">No posts yet — check back soon.</li>
  {% endif %}
</ul>
