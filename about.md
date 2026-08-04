---
layout: default
title: About
permalink: /about/
keywords:
  - Human-Centered AI
  - Machine Learning
  - Product Thinking
  - Writing
---

<main>
  <section id="about" class="section section-muted page-section">
    <div class="container two-column">
      <div class="section-heading reveal">
        <p class="eyebrow">About</p>
        <h1 class="page-title">About Me</h1>
      </div>
      <div class="content-card reveal" markdown="1">
Use this section to describe your education, research interests, current work, and long-term goals.
A concise two- or three-paragraph introduction helps visitors quickly understand who you are and what you do.

For example: I am interested in human-centered AI systems and data-driven decision making,
with a focus on research and product development that can be applied to real-world problems.

<ul class="tag-list" aria-label="Keywords">
{% for keyword in page.keywords %}
  <li>{{ keyword }}</li>
{% endfor %}
</ul>
      </div>
    </div>
  </section>

  <section id="news" class="section">
    <div class="container">
      <div class="section-heading reveal">
        <p class="eyebrow">News</p>
        <h2>Recent News</h2>
      </div>
      <div class="timeline reveal">
        {% assign news_items = site.news | sort: 'date' | reverse %}
        {% for item in news_items %}
        <article class="timeline-item">
          <time datetime="{{ item.date | date: '%Y-%m' }}">{{ item.label | default: item.date }}</time>
          <p>{{ item.content | markdownify | remove: '<p>' | remove: '</p>' }}</p>
        </article>
        {% endfor %}
      </div>
    </div>
  </section>
</main>
