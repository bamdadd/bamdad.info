---
layout: page
title: Blog
permalink: /blog/
---

<div class="content-section">
  <div class="wrapper">
    <div class="section-title">
      <h2>Technical Insights & Case Studies</h2>
      <p class="section-subtitle">Deep-dive articles on AI, software engineering, DevOps, and compliance in regulated industries</p>
    </div>
    
    <div class="post-list">
      {%- for post in site.posts -%}
      <article class="post-item">
        <div class="post-meta">
          <span class="post-category">{{ post.categories | first | capitalize }}</span>
          <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%B %d, %Y" }}</time>
        </div>
        <h3><a href="{{ post.url | relative_url }}">{{ post.title | escape }}</a></h3>
        {%- if post.excerpt -%}
          <div class="post-excerpt">{{ post.excerpt | strip_html | truncatewords: 40 }}</div>
        {%- endif -%}
        <div class="read-more">
          <a href="{{ post.url | relative_url }}" class="btn btn-primary">Read Article</a>
        </div>
      </article>
      {%- endfor -%}
    </div>
  </div>
</div>

<style>
.read-more {
  margin-top: 1.5rem;
}

.read-more .btn {
  font-size: 0.9rem;
  padding: 0.5rem 1rem;
}
</style>