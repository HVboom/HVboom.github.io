---
title: Jekyll Setup Guide
nav_order: 2
last_modified_date: 2025-07-15
---

## Jekyll Setup

1. Fork or clone this repository.
2. Ensure `_config.yml` contains `remote_theme: pages-themes/cayman@v0.2.0`.
   ```yml
   remote_theme: pages-themes/cayman@v0.2.0
   plugins:
     - jekyll-remote-theme # add this line to the plugins list if you already have one
  ```
3. Add `CNAME` file with your domain (e.g. `hvboom.org`).
4. Push to `main` branch to trigger GitHub Pages.
5. Optionally test locally:  
   ```bash
   bundle install
   bundle exec jekyll serve
   ```
