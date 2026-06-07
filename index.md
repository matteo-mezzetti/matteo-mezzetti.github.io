---
layout: default
title: Home
---

<div class="hero">
  <p class="greeting">Hi, I'm</p>
  <h1>Matteo Mezzetti</h1>
  <p>2nd year B.Commerce student at UQ studying Business Analytics and Business Information Systems. I build things with R, SQL, and Python — ask me what I've broken lately.</p>
  <div class="tags">
    <span class="tag">R</span>
    <span class="tag">SQL</span>
    <span class="tag">Python</span>
    <span class="tag">Excel</span>
    <span class="tag">Google Workspace</span>
  </div>
  <p>📫 <a href="https://linkedin.com">Connect on LinkedIn</a> — send a note and I'll accept.</p>
</div>

## Recent Projects

**[Unified Team Intranet →](/projects)**  
Centralised Google Workspace intranet for a 100+ person student organisation, replacing 6 siloed team drives.

## From the Blog

{% for post in site.posts limit:3 %}
- [{{ post.title }}]({{ post.url | relative_url }}) — <span style="color: var(--muted); font-size: 0.88rem;">{{ post.date | date: "%b %-d, %Y" }}</span>
{% endfor %}
{% if site.posts.size == 0 %}
*No posts yet — check back soon.*
{% endif %}
