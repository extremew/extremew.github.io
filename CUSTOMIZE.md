# 🚀 Quick Start & Customization Guide

Your Jekyll tech portfolio is ready! Here's how to customize it with your own information.

## 🎯 Quick Setup (First Steps)

### 1. Update Site Configuration
Edit `_config.yml`:
```yaml
title: "Your Portfolio Title"
author: "Your Name"
url: "https://yourusername.github.io"

social_links:
  github: yourusername
  linkedin: yourusername
  twitter: yourusername
```

### 2. Update Home Page
Edit `index.md` and change "Your Name" to your actual name throughout.

### 3. Update About Page
Edit `_pages/about.md` with your bio, mission, and personal info.

### 4. Update Tech Stack
Edit `_pages/tech-stack.md` with the technologies **you** actually use. Use the emoji guide at the bottom of [EMOJI_GUIDE.md](EMOJI_GUIDE.md) for consistency.

---

## ✏️ How to Add Your Own Content

### Add a New Project

Create a file in `_projects/project-name.md`:

```markdown
---
layout: project
title: "Your Project Name"
description: "Brief description of what it does"
permalink: /portfolio/project-name/
tech_stack:
  - "⚛️ React"
  - "🔌 Node.js"
  - "📘 PostgreSQL"
links:
  github: "https://github.com/yourusername/project"
  live: "https://project-demo.com"
  blog: "/blog/2026/05/23/project-post/"
---

## Project Overview
Your detailed project description...

### Key Features
- Feature 1
- Feature 2

### Technical Highlights
...
```

### Add a Blog Post

Create a file in `_posts/YYYY-MM-DD-title.md`:

```markdown
---
layout: post
title: "Your Blog Title"
date: 2026-05-23
categories: [Category1, Category2]
tags: [tag1, tag2]
excerpt: "Brief excerpt shown in blog list"
---

## Section Heading
Your blog content here...
```

**Date Format**: Files MUST be named `YYYY-MM-DD-title.md` for Jekyll to recognize them as posts.

---

## 🎨 Customize Colors

Edit `_sass/_variables.scss` to change the Ayu Dark palette:

```scss
$ayu-primary: #FF8F40;      // Change to your primary color
$ayu-secondary: #AAD94C;    // Change secondary accent
$ayu-tertiary: #39BAE6;     // Change link/interactive color
$ayu-background: #0F1419;   // Change background
$ayu-foreground: #E6E1CF;   // Change text color
```

After changes, Jekyll automatically rebuilds (when running `bundle exec jekyll serve`).

---

## 📸 Add Images to Projects

1. Place images in `assets/images/`
2. Reference in markdown:
```markdown
![Alt text]({{ site.baseurl }}/assets/images/image-name.png)
```

---

## 🚀 Deploy to GitHub Pages

### Option 1: Username Repository (Easiest)
```bash
# Create repo: yourusername.github.io
git init
git add .
git commit -m "Initial Jekyll portfolio"
git branch -M main
git remote add origin https://github.com/yourusername/yourusername.github.io.git
git push -u origin main
```
Site auto-deploys to: https://yourusername.github.io

### Option 2: Project Repository
Same as above, but push to any repo name. Then go to:
- Settings → Pages
- Select `main` branch as source
- Site builds to: https://yourusername.github.io/repo-name/

---

## 🔧 Local Development

### Start Server
```bash
bundle exec jekyll serve
```
Visit: http://localhost:4000

### Rebuild CSS
```bash
bundle exec jekyll clean
bundle exec jekyll build
```

### Update Dependencies
```bash
bundle update
```

---

## 💡 Tips & Tricks

### Emojis Work Everywhere
Use GitHub emoji shortcodes in markdown:
- `:rocket:` → 🚀
- `:star:` → ⭐
- `:tada:` → 🎉

See [EMOJI_GUIDE.md](EMOJI_GUIDE.md) for common tech emoji codes.

### Front Matter is Important
All markdown files need front matter (YAML between `---`):
```markdown
---
layout: post
title: "Title"
date: 2026-05-23
---
```

### Preview Changes Locally
Always run `bundle exec jekyll serve` before pushing to verify:
- All posts appear
- Navigation works
- Links are correct
- Images display properly

### Use Relative Paths
Always use `{{ site.baseurl }}` for links:
```markdown
[Link]({{ site.baseurl }}/about/)
```

---

## 🛠️ Common Tasks

| Task | Command |
|------|---------|
| Start dev server | `bundle exec jekyll serve` |
| Full rebuild | `bundle exec jekyll clean && bundle exec jekyll build` |
| Update gems | `bundle update` |
| Check for issues | `bundle audit` |

---

## ❓ Troubleshooting

**Posts not showing?**
- Check filename format: `YYYY-MM-DD-title.md`
- Ensure front matter is valid YAML
- Check `_config.yml` has `jekyll-feed` plugin

**Links broken?**
- Use `{{ site.baseurl }}` in all links
- Check `_config.yml` url and baseurl settings

**Styles not showing?**
- Run: `bundle exec jekyll clean`
- Then: `bundle exec jekyll serve`
- Refresh browser hard refresh: Ctrl+Shift+R

**Can't run Jekyll?**
- Run: `bundle install`
- Run: `bundle exec jekyll serve`

---

## 📚 Learn More

- [Jekyll Docs](https://jekyllrb.com/docs/)
- [Thinkspace Theme](https://github.com/heiswayi/thinkspace)
- [Markdown Guide](https://www.markdownguide.org/)
- [GitHub Pages Guide](https://pages.github.com/)

---

**Happy customizing! 🎉**

*Don't forget to update your social links and customize the colors to match your personal brand!*
