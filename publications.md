---
layout: default
title: Publications
permalink: /publications/
---

<main>
  <section id="publications" class="section section-muted page-section">
    <div class="container">
      <div class="section-heading reveal">
        <p class="eyebrow">Publication</p>
        <h1 class="page-title">Publications</h1>
      </div>
      <div class="publication-list reveal">
        {% assign publications = site.publications | sort: 'year' | reverse %}
        {% for publication in publications %}
        <article class="publication-item">
          <div class="publication-year">{{ publication.year }}</div>
          <div>
            <h3>{{ publication.title }}</h3>
            <p class="authors">{{ publication.authors }}</p>
            <p class="venue">{{ publication.venue }}</p>
            <div class="item-links">
              {% for link in publication.links %}
              <a href="{{ link.url }}">{{ link.label }}</a>
              {% endfor %}
            </div>
          </div>
        </article>
        {% endfor %}
      </div>
    </div>
  </section>
</main>
