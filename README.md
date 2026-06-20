# Tech & Learning Lab

A modern, minimalist tech and learning blog with portfolio, built with Jekyll and Ayu Dark theme.

## 🎨 Features

- **Minimalist Design**: Clean, distraction-free reading experience
- **Ayu Dark Theme**: Modern dark color scheme optimized for eye comfort
- **Responsive**: Mobile-friendly design
- **Fast**: Static site generation with Jekyll
- **SEO Optimized**: Built-in Jekyll SEO tag plugin
- **Blog**: In-depth articles about tech and learning
- **Portfolio**: Showcase your projects and work
- **Services**: Describe your offerings and expertise

## 📋 Color Scheme (Ayu Dark)

```
Background:      #0D1117
Surface:         #161B22
Text:            #B3B1AD
Accent (Cyan):   #5CCFE6
Accent (Orange): #FFD580
Border:          #30363D
```

## 🚀 Quick Start

### Prerequisites
- Ruby 2.7+
- Bundler

### Installation

```bash
# Clone or navigate to your project
cd jekyll

# Install dependencies
bundle install

# Build the site
bundle exec jekyll build

# Serve locally
bundle exec jekyll serve
```

Then open [http://localhost:4000](http://localhost:4000)

## 📁 Project Structure

```
jekyll/
├── _layouts/              # HTML templates
│   ├── default.html      # Main layout
│   ├── home.html         # Homepage
│   ├── post.html         # Blog post template
│   ├── page.html         # Static pages
│   └── portfolio-item.html # Portfolio items
├── _sass/
│   └── custom.scss       # Ayu Dark theme styles
├── _posts/               # Blog posts (Markdown)
├── _portfolio/           # Portfolio projects
├── assets/
│   ├── css/style.scss    # Main stylesheet
│   └── images/           # Image assets
├── _config.yml           # Site configuration
├── Gemfile               # Ruby dependencies
├── index.md              # Homepage
├── blog.md               # Blog index
├── portfolio.md          # Portfolio index
├── about.md              # About page
└── services.md           # Services page
```

## ✏️ Customization

### Update Site Information

Edit `_config.yml`:
```yaml
title: Your Blog Title
tagline: Your tagline
author:
  name: Your Name
  email: your.email@example.com
url: "https://yourusername.github.io"
```

### Add a Blog Post

Create a new file in `_posts/` with the naming convention `YYYY-MM-DD-title.md`:

```markdown
---
layout: post
title: "Your Post Title"
date: 2024-06-11 10:30:00 -0400
categories: category
tags: [tag1, tag2]
author: Your Name
---

Your content here...
```

### Add a Portfolio Item

Create a new file in `_portfolio/`:

```markdown
---
layout: portfolio-item
title: "Project Name"
date: 2024-06-11
categories: category
tags: [tech1, tech2]
---

Project description...
```

### Modify Colors

Edit `_sass/custom.scss` to customize the Ayu Dark theme colors at the top of the file.

## 🚢 Deployment to GitHub Pages

### Setup

1. Create a GitHub repository named `yourusername.github.io`
2. Push your Jekyll project to the `main` branch
3. GitHub automatically builds and deploys to `https://yourusername.github.io`

### Configure

```yaml
# In _config.yml
url: "https://yourusername.github.io"
baseurl: ""
```

## 📚 Content Guidelines

### Blog Posts
- Use clear, descriptive titles
- Include relevant categories and tags
- Add metadata (date, author, etc.)
- Use code blocks for examples
- Link to relevant resources

### Portfolio Projects
- Highlight key achievements
- List technologies used
- Include project links
- Add visual descriptions

## 🔧 Technologies Used

- **Static Generator**: Jekyll 3.9+
- **Language**: Markdown
- **Styling**: SCSS
- **Theme**: Custom (based on Ayu Dark)
- **Hosting**: GitHub Pages
- **Plugins**:
  - jekyll-feed (RSS feed)
  - jekyll-seo-tag (SEO optimization)

## 📦 Plugins

The following Jekyll plugins are enabled:

- `jekyll-feed`: Automatically generates feed.xml for RSS
- `jekyll-seo-tag`: Adds SEO meta tags

## 🌐 Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Mobile browsers

## ⚙️ Build & Deployment

### Local Development

```bash
# Watch for changes and rebuild
bundle exec jekyll serve --watch

# Build only
bundle exec jekyll build

# Build for production
JEKYLL_ENV=production bundle exec jekyll build
```

### GitHub Pages Deployment

Push to `main` branch:
```bash
git add .
git commit -m "Update blog"
git push origin main
```

GitHub automatically deploys after you push.

## 📝 License

This project is open source and available under the MIT License.

## 🤝 Contributing

Contributions are welcome! Feel free to submit issues and pull requests.

## 📧 Contact

- Email: your.email@example.com
- GitHub: [@yourusername](https://github.com/yourusername)
- Twitter: [@yourhandle](https://twitter.com/yourhandle)

---

**Built with ❤️ using Jekyll and Ayu Dark theme**
