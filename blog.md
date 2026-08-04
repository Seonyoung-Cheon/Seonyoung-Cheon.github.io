---
layout: default
title: Blog
permalink: /blog/
---

<main>
  <section id="blog" class="section section-muted page-section">
    <div class="container">
      <div class="section-heading reveal">
        <p class="eyebrow">Blog</p>
        <h1 class="page-title">Blog</h1>
      </div>
      <div class="blog-grid reveal">
        {% for post in site.posts %}
        <article class="blog-card">
          <time datetime="{{ post.date | date: '%Y-%m-%d' }}">{{ post.date | date: "%Y.%m.%d" }}</time>
          <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
          <p>{{ post.excerpt | strip_html | truncate: 90 }}</p>
          <a class="read-more" href="{{ post.url | relative_url }}">Read more</a>
        </article>
        {% endfor %}
      </div>
    </div>
  </section>
</main>
