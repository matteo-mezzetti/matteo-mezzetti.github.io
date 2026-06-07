---
layout: default
title: Home
---

<div class="hero">
  <p class="hero-eyebrow">B.Commerce · UQ · Brisbane</p>
  <h1>Building things with data.</h1>
  <p>Business Analytics &amp; Information Systems student. I work with R, SQL, and Python — ask me what I've broken lately.</p>
  <div class="tags">
    <span class="tag">R</span>
    <span class="tag">SQL</span>
    <span class="tag">Python</span>
    <span class="tag">Excel</span>
    <span class="tag">Google Workspace</span>
  </div>
  <a href="https://linkedin.com" class="cta">📫 Connect on LinkedIn</a>
</div>

<div class="section">
  <p class="section-title">Projects</p>
  <div class="item-row">
    <a href="/projects" class="item-link">Unified Team Intranet →</a>
    <p class="item-desc">Centralised Google Workspace intranet for a 100+ person student org, replacing 6 siloed team drives.</p>
  </div>
</div>

<div class="section">
  <p class="section-title">Writing</p>
  {% for post in site.posts limit:3 %}
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
