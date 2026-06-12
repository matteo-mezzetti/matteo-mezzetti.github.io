---
layout: default
title: Home
description: Matteo Mezzetti — Business Analytics & Information Systems student at UQ. Projects in R, SQL, Python, and Google Workspace.
---

<div class="hero">
  <p class="hero-eyebrow">B.Commerce · UQ · Brisbane</p>
  <h1>Building things with data.<span class="cursor"></span></h1>
  <p>I'm Matteo — a Business Analytics &amp; Information Systems student who likes turning messy data and messier processes into something useful. Currently working in R, SQL, and Python.</p>
  <div class="tags">
    <span class="tag">R</span>
    <span class="tag">SQL</span>
    <span class="tag">Python</span>
    <span class="tag">Excel</span>
    <span class="tag">Google Workspace</span>
  </div>
  <div class="cta-row">
    <a href="https://www.linkedin.com/in/matteo-mezzetti/" class="cta">Connect on LinkedIn</a>
    <a href="mailto:matteomezzetti7@gmail.com" class="cta-secondary">Email me →</a>
  </div>
</div>

<div class="section">
  <p class="section-title">Featured project</p>
  <div class="item-row">
    <a href="/projects" class="item-link">Unified Team Intranet →</a>
    <p class="item-desc">Centralised Google Workspace intranet for a 100+ person student org, replacing 6 siloed team drives with one source of truth.</p>
  </div>
  <div class="item-row">
    <a href="/projects" class="item-link">Predicting Song Hotness <span class="badge badge-wip">In progress</span></a>
    <p class="item-desc">Can audio features predict a hit? Exploring the Million Song Dataset with R and SQL.</p>
  </div>
  <div class="item-row">
    <a href="/projects" class="item-link">Vineyard Management Database <span class="badge badge-wip">In progress</span></a>
    <p class="item-desc">Relational database design for vineyard operations — from ER model to working queries.</p>
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
