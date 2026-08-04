---
layout: default
title: Home
keywords:
  - Human-Centered AI
  - Machine Learning
  - Product Thinking
  - Writing
---

<main id="home">
  <section class="hero section">
    <div class="container hero-grid">
      <div class="hero-content reveal">
        <p class="eyebrow">Personal Homepage</p>
        <h1>Hello, I’m <span>{{ site.title }}</span>.</h1>
        <p class="hero-description">
          I am interested in solving meaningful problems through research, development, and writing.
          This website highlights my background, recent news, publications, recognition, and blog posts.
        </p>
        <div class="hero-actions">
          <a class="button" href="#publications">View Publications</a>
          <a class="button button-secondary" href="#blog">Read Blog</a>
        </div>
        <div class="social-links" aria-label="Social links">
          <a href="{{ site.social.github }}" target="_blank" rel="noreferrer">GitHub</a>
          <a href="{{ site.social.scholar }}" target="_blank" rel="noreferrer">Scholar</a>
          <a href="{{ site.social.linkedin }}" target="_blank" rel="noreferrer">LinkedIn</a>
        </div>
      </div>
      <aside class="profile-card reveal" aria-label="Profile summary">
        <div class="profile-image" role="img" aria-label="Profile placeholder">{{ site.initials }}</div>
        <h2>{{ site.title }}</h2>
        <p>{{ site.profile.role }}</p>
        <dl>
          <div>
            <dt>Interest</dt>
            <dd>{{ site.profile.interests }}</dd>
          </div>
          <div>
            <dt>Affiliation</dt>
            <dd>{{ site.profile.affiliation }}</dd>
          </div>
          <div>
            <dt>Location</dt>
            <dd>{{ site.profile.location }}</dd>
          </div>
        </dl>
      </aside>
    </div>
  </section>

  <section id="about" class="section section-muted">
    <div class="container two-column">
      <div class="section-heading reveal">
        <p class="eyebrow">About</p>
        <h2>About Me</h2>
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

  <section id="publications" class="section section-muted">
    <div class="container">
      <div class="section-heading reveal">
        <p class="eyebrow">Publication</p>
        <h2>Publications</h2>
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

  <section id="recognition" class="section">
    <div class="container">
      <div class="section-heading reveal">
        <p class="eyebrow">Recognition</p>
        <h2>Recognition</h2>
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

  <section id="blog" class="section section-muted">
    <div class="container">
      <div class="section-heading reveal">
        <p class="eyebrow">Blog</p>
        <h2>Blog</h2>
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
