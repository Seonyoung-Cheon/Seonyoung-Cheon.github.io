# Personal Homepage

A personal homepage built with GitHub Pages and Jekyll. The site is structured so that most content can be edited by writing Markdown files.

## What should I edit?

### 1. Basic information

Update your name, initials, email address, affiliation, interests, and social links in `_config.yml`.

```yml
title: Your Name
initials: YN
email: your.email@example.com
```

### 2. Homepage and About section

Edit the main introduction and About section in `index.md`.

### 3. Add News items

Add Markdown files to the `_news/` folder.

Example: `_news/2026-08-new-paper.md`

```md
---
date: 2026-08-04
label: Aug 2026
---

My new paper was accepted to a conference.
```

### 4. Add Publications

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

### 5. Add Recognition items

Add Markdown files to the `_recognitions/` folder.

Example: `_recognitions/2026-award.md`

```md
---
title: Award or Activity Name
year: 2026
---

Describe the organization, presentation, award, or activity.
```

### 6. Add Blog posts

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
index.md                 # Homepage content
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

The site is not completely HTML-free. Jekyll still uses HTML templates in `_layouts` and `_includes`. However, day-to-day content updates can be handled through `index.md`, `_news`, `_publications`, `_recognitions`, and `_posts`.
