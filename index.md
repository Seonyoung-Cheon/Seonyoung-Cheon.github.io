---
layout: default
title: Home
---

<main id="home">
  <section class="hero section">
    <div class="container hero-grid hero-grid-profile-left">
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

      <div class="hero-content reveal">
        <p class="eyebrow">Personal Homepage</p>
        <h1>Hello, I’m <span>{{ site.title }}</span>.</h1>
        <p class="hero-description">
          I am interested in solving meaningful problems through research, development, and writing.
          This website highlights my background, recent news, publications, recognition, and blog posts.
        </p>
        <div class="hero-actions">
          <a class="button" href="{{ '/about/' | relative_url }}">About Me</a>
          <a class="button button-secondary" href="{{ '/publications/' | relative_url }}">View Publications</a>
        </div>
        <div class="social-links" aria-label="Social links">
          <a href="{{ site.social.github }}" target="_blank" rel="noreferrer">GitHub</a>
          <a href="{{ site.social.scholar }}" target="_blank" rel="noreferrer">Scholar</a>
          <a href="{{ site.social.linkedin }}" target="_blank" rel="noreferrer">LinkedIn</a>
        </div>
      </div>
    </div>
  </section>
</main>
