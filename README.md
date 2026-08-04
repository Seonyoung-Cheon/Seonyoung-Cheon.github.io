# Personal Homepage

A personal homepage built with GitHub Pages and Jekyll. The site is organized as separate pages, and most content can be edited by writing Markdown files.

## Pages

- `index.md`: Home
- `about.md`: About and News
- `publications.md`: Publications
- `recognition.md`: Recognition
- `blog.md`: Blog list
- `_posts/*.md`: Individual blog posts

## What should I edit?

### 1. Basic information

Update your name, initials, email address, affiliation, interests, and social links in `_config.yml`.

```yml
title: Your Name
initials: YN
email: your.email@example.com
```

### 2. Homepage

Edit the homepage introduction in `index.md`.

### 3. About and News

Edit the About section text in `about.md`.

Add News items by creating Markdown files in the `_news/` folder.

Example: `_news/2026-08-new-paper.md`

```md
---
date: 2026-08-04
label: Aug 2026
---

My new paper was accepted to a conference.
```

### 4. Publications

Add Markdown files to the `_publications/` folder.

Example: `_publications/2026-paper-title.md`

```md
---
title: Paper Title
year: 2026
authors: <strong>Your Name</strong>, Co-author
venue: Conference / Journal Name
links:
  - label: Paper
    url: https://example.com
  - label: Code
    url: https://github.com/example/repo
---
```

### 5. Recognition

Add Markdown files to the `_recognitions/` folder.

Example: `_recognitions/2026-award.md`

```md
---
title: Award or Activity Name
year: 2026
---

Describe the organization, presentation, award, or activity.
```

### 6. Blog posts

Add Markdown files to `_posts/` using the `YYYY-MM-DD-title.md` format.

```md
---
layout: post
title: Post Title
date: 2026-08-04
reading_time: 3 min read
---

Write the body in Markdown.
```

## File structure

```text
_config.yml              # Site-wide settings
index.md                 # Home page
about.md                 # About and News page
publications.md          # Publications page
recognition.md           # Recognition page
blog.md                  # Blog list page
_news/*.md               # News items
_publications/*.md       # Publication items
_recognitions/*.md       # Recognition items
_posts/*.md              # Blog posts
_layouts/*.html          # Jekyll layouts; usually no need to edit
_includes/*.html         # Shared header/footer; usually no need to edit
assets/css/styles.css    # Design styles
assets/js/main.js        # Mobile menu and subtle reveal effect
assets/images/           # Image files
```

## Deploy with GitHub Pages

1. Create a GitHub repository named `<username>.github.io`.
2. Push the files in this folder to the root of that repository.
3. Go to Repository Settings → Pages.
4. Select `Deploy from a branch`.
5. Choose the `main` branch and `/root` folder.
6. After a short while, visit `https://<username>.github.io`.

## Note

The site is not completely HTML-free. Jekyll still uses HTML templates in `_layouts` and `_includes`. However, day-to-day content updates can be handled through Markdown files such as `index.md`, `about.md`, `_news`, `_publications`, `_recognitions`, and `_posts`.
