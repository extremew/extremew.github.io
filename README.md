# 💻 Tech Portfolio - Jekyll Site with Thinkspace + Ayu

A modern, minimalist tech portfolio and learning blog built with Jekyll, Thinkspace theme, and Ayu Dark color scheme.

![Theme](https://img.shields.io/badge/Theme-Thinkspace-blue)
![Colors](https://img.shields.io/badge/Colors-Ayu%20Dark-purple)
![Jekyll](https://img.shields.io/badge/Jekyll-4.3.0-red)
![License](https://img.shields.io/badge/License-MIT-green)

## 🎯 Features

### 📂 Core Sections
- **🚀 Portfolio**: Showcase your projects with tech stack badges and links
- **📚 Learning Journey**: Blog posts documenting your tech learning experiences
- **🛠️ Tech Stack**: Comprehensive overview of technologies and tools you use
- **👤 About**: Personal bio and mission statement
- **🏠 Home**: Hero section with featured projects and latest posts

### 🎨 Design
- **Dark Theme**: Ayu Dark color palette for professional, comfortable viewing
- **Emoji Integration**: GitHub-style emojis throughout the site using jemoji
- **Responsive Design**: Mobile-friendly layout that works on all devices
- **Minimalist Layout**: Clean, focused design inspired by Thinkspace theme
- **Interactive Elements**: Hover effects and smooth transitions

### ⚙️ Technology Stack
- **Jekyll**: Static site generator
- **Thinkspace**: Minimalist Jekyll theme
- **Ayu Dark**: Professional color scheme
- **jemoji**: GitHub-flavored emoji support
- **SEO**: Built-in jekyll-seo-tag for social sharing
- **Responsive**: Mobile-first design approach

## 📋 Prerequisites

- Ruby 2.4.0 or later
- Bundler (`gem install bundler`)
- Git (for version control)

## 🚀 Quick Start

### 1. Clone/Setup
```bash
cd /home/reiser/Projects/Portfolio
```

### 2. Install Dependencies
```bash
bundle install
```

### 3. Local Development
```bash
bundle exec jekyll serve
```
Visit `http://localhost:4000` in your browser

### 4. Build for Production
```bash
bundle exec jekyll build
```
Output goes to `_site/` directory

## 📁 Project Structure

```
Portfolio/
├── _config.yml              # Jekyll configuration
├── _sass/
│   ├── _variables.scss      # Ayu Dark colors & settings
│   └── main.scss            # Base styles
├── _layouts/
│   ├── default.html         # Base layout with header/footer
│   ├── page.html            # Static page layout
│   ├── post.html            # Blog post layout
│   └── project.html         # Project showcase layout
├── _includes/
│   ├── header.html          # Navigation header
│   └── footer.html          # Footer with social links
├── _posts/                  # Blog posts (Learning Journey)
├── _projects/               # Portfolio projects
├── _pages/                  # Static pages (About, Tech Stack)
├── assets/
│   ├── css/
│   │   ├── style.scss       # Main stylesheet entry
│   │   └── main.scss        # CSS compilation target
│   └── images/              # Project images and assets
├── Gemfile                  # Ruby dependencies
├── index.md                 # Home page
└── EMOJI_GUIDE.md           # Emoji reference
```

## ✏️ Customization

### Update Site Info
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

### Change Colors
Edit `_sass/_variables.scss` to modify Ayu Dark colors:
```scss
$ayu-primary: #FF8F40;      // Primary accent color
$ayu-background: #0F1419;   // Background color
$ayu-foreground: #E6E1CF;   // Text color
```

### Add Projects
Create new file in `_projects/`:
```markdown
---
layout: project
title: "Project Name"
description: "Brief description"
tech_stack:
  - "⚛️ React"
  - "🔵 TypeScript"
links:
  github: "https://github.com/..."
  live: "https://demo.com"
---

## Project Details
Your content here...
```

### Add Blog Posts
Create new file in `_posts/YYYY-MM-DD-title.md`:
```markdown
---
layout: post
title: "Post Title"
date: 2026-05-23
categories: [Category1, Category2]
tags: [tag1, tag2]
excerpt: "Brief excerpt for preview"
---

## Content
Your blog post content here...
```

## 🌐 Deploying to GitHub Pages

### Option 1: Username Repository (Automatic)
1. Create repo named `{username}.github.io`
2. Push code to `main` branch
3. GitHub automatically builds and deploys

### Option 2: Project Repository
1. Create any repository
2. Go to Settings → Pages
3. Select `main` branch as source
4. Site deploys to `{username}.github.io/{repo-name}`

### Option 3: Custom Domain
1. Update `_config.yml` with your domain
2. Add CNAME file to root with domain name
3. Configure DNS records on domain registrar

## 🛠️ Maintenance

### Update Dependencies
```bash
bundle update
```

### Clean Build
```bash
bundle exec jekyll clean
bundle exec jekyll build
```

### Check for Issues
```bash
bundle audit
```

## 📚 Learning Resources

- [Jekyll Documentation](https://jekyllrb.com/docs/)
- [Thinkspace Theme](https://github.com/heiswayi/thinkspace)
- [Ayu Color Scheme](https://ayutheme.com/)
- [GitHub Pages Guide](https://pages.github.com/)
- [Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)

## 📊 Ayu Color Reference

**Ayu Dark Palette:**
- Background: `#0F1419`
- Foreground: `#E6E1CF`
- Primary (Orange): `#FF8F40`
- Secondary (Green): `#AAD94C`
- Tertiary (Blue): `#39BAE6`
- Comment (Gray): `#626A73`

## 🤝 Contributing

This is your personal portfolio! Feel free to:
- Add more projects
- Write more blog posts
- Customize colors and layouts
- Experiment with new features

## 📝 License

This project uses the MIT License. Feel free to use it as a template for your own portfolio!

## 🙏 Acknowledgments

- **Jekyll**: For the amazing static site generator
- **Heiswayi Nreza**: Creator of Thinkspace theme
- **Ayu Theme Team**: For the beautiful color palette
- **GitHub Pages**: For free hosting

## 🚀 Next Steps

1. ✅ Install dependencies: `bundle install`
2. ✅ Test locally: `bundle exec jekyll serve`
3. ✅ Customize with your info and projects
4. ✅ Deploy to GitHub Pages
5. ✅ Share with the world! 🌍

---

**Built with ❤️ using Jekyll + Thinkspace + Ayu**

*Last Updated: May 2026*
