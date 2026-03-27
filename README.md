# Knocking Tin — knockingtin.com

HVAC fabrication knowledge, from the shop floor.

## Setup

### 1. Create a GitHub repository
- Go to github.com → New repository
- Name it `knockingtin` (or anything you like)
- Set it to **Public**
- Do NOT initialize with a README (you already have one)

### 2. Push this folder to GitHub
Open a terminal in this folder and run:

```bash
git init
git add .
git commit -m "Initial site"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/knockingtin.git
git push -u origin main
```

### 3. Enable GitHub Pages
- Go to your repo → Settings → Pages
- Source: **Deploy from a branch**
- Branch: `main` / `/ (root)`
- Click Save

Your site will be live at `https://YOUR_USERNAME.github.io/knockingtin` within a few minutes.

### 4. Connect your custom domain
- In GitHub Pages settings, enter `knockingtin.com` in the Custom Domain field
- At your domain registrar (GoDaddy, Namecheap, etc.), add these DNS records:

```
Type    Host    Value
A       @       185.199.108.153
A       @       185.199.109.153
A       @       185.199.110.153
A       @       185.199.111.153
CNAME   www     YOUR_USERNAME.github.io
```

DNS changes can take up to 48 hours to propagate. GitHub will automatically provision an SSL certificate once the domain resolves.

---

## Writing a New Post

1. Create a new file in `_posts/` named: `YYYY-MM-DD-your-post-title.md`
2. Copy this header to the top of the file:

```yaml
---
layout: post
title: "Your Post Title Here"
description: "One sentence summary — shows on homepage and in Google."
category: Fabrication Fundamentals
date: 2025-04-01
read_time: 7
featured: false
tags: [tag1, tag2, tag3]
---
```

3. Write your article below the `---` line using Markdown.
4. Save, commit, and push to GitHub. The site rebuilds automatically.

### Featured post
Set `featured: true` on ONE post to make it appear in the large hero slot on the homepage. Set all others to `featured: false`.

### Markdown quick reference
```
## Big heading
### Smaller heading

Normal paragraph text. **Bold text.** *Italic text.*

- Bullet list item
- Another item

1. Numbered list
2. Second item

[Link text](https://example.com)

> Blockquote for a key point or quote
```

---

## File Structure

```
knockingtin/
├── _config.yml          ← Site settings (title, author, URLs)
├── _layouts/
│   ├── default.html     ← Nav + footer wrapper for all pages
│   └── post.html        ← Article page template
├── _posts/              ← Your articles go here (one .md file each)
├── assets/
│   └── css/
│       └── main.css     ← All styles
├── blog.html            ← Blog index page
├── index.html           ← Homepage
└── Gemfile              ← Ruby dependencies (don't edit)
```
