---
title: Custom Domain Setup with DigitalOcean
layout: default
---

# 🌐 Setup GitHub Pages with DigitalOcean DNS

This guide helps you configure your domain `hvboom.biz` at DigitalOcean to point to your GitHub Pages site.

## Step 1: Prepare GitHub

1. Add a file named `CNAME` to the root of your GitHub repository (`hvboom.github.io`) with:
   ```
   hvboom.biz
   ```

2. Commit and push:
   ```bash
   git add CNAME
   git commit -m "Add custom domain"
   git push
   ```

3. Go to your repository → ⚙️ Settings → Pages:
   - Set “Custom Domain” to `hvboom.biz`
   - Enable “Enforce HTTPS”

## Step 2: Configure DNS on DigitalOcean

1. Go to [DigitalOcean DNS](https://cloud.digitalocean.com/networking/domains)
2. Add a domain: `hvboom.biz`
3. Under Records, add the following:

### A Records for root domain (`hvboom.biz`):

| Type | Hostname | Value |
|------|----------|-------|
| A    | `@`      | `185.199.108.153` |
| A    | `@`      | `185.199.109.153` |
| A    | `@`      | `185.199.110.153` |
| A    | `@`      | `185.199.111.153` |

### CNAME for `www`:

| Type  | Hostname | Value               |
|-------|----------|---------------------|
| CNAME | `www`    | `hvboom.github.io.` |

## Step 3: Wait and Verify

- DNS propagation may take several hours
- Visit [https://hvboom.biz](https://hvboom.biz) to verify
- GitHub Pages will show a green lock when HTTPS is ready
