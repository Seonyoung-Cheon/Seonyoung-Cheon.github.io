---
layout: default
title: Recognition
permalink: /recognition/
---

<main>
  <section id="recognition" class="section page-section">
    <div class="container">
      <div class="section-heading reveal">
        <p class="eyebrow">Recognition</p>
        <h1 class="page-title">Recognition</h1>
      </div>
      <div class="cards-grid reveal">
        {% assign recognitions = site.recognitions | sort: 'year' | reverse %}
        {% for item in recognitions %}
        <article class="info-card">
          <span class="card-date">{{ item.year }}</span>
          <h3>{{ item.title }}</h3>
          <p>{{ item.content | markdownify | strip_html }}</p>
        </article>
        {% endfor %}
      </div>
    </div>
  </section>
</main>
