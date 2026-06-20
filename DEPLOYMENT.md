# Deployment Guide

This guide explains how to deploy your Tech & Learning Lab blog to GitHub Pages.

## Prerequisites

- GitHub account
- Git installed locally
- Your Jekyll blog setup (this repository)

## Step 1: Create a GitHub Repository

1. Go to [GitHub](https://github.com/new)
2. Create a new repository named: `yourusername.github.io`
   - Replace `yourusername` with your GitHub username
3. Choose "Public" (required for GitHub Pages)
4. Do **not** initialize with README (we have one)

## Step 2: Configure Your Blog

Update `_config.yml` with your actual information:

```yaml
title: Tech & Learning Lab
tagline: Your tagline
author:
  name: Your Name
  email: your.email@example.com

url: "https://yourusername.github.io"
baseurl: ""

twitter:
  username: your_twitter

social:
  name: Your Name
  links:
    - https://twitter.com/your_twitter
    - https://github.com/yourusername
    - https://linkedin.com/in/yourprofile
```

Update contact information in:
- `about.md`
- `services.md`
- `_layouts/default.html` (footer links)

## Step 3: Initialize Git & Push

From your project directory:

```bash
# Initialize git repository
git init

# Add all files
git add .

# Create initial commit
git commit -m "Initial commit: Tech & Learning Lab blog"

# Add remote repository
git remote add origin https://github.com/yourusername/yourusername.github.io.git

# Push to GitHub
git push -u origin main
```

Note: If your default branch is `master` instead of `main`:
```bash
git push -u origin master
```

## Step 4: Enable GitHub Pages

1. Go to your repository: `https://github.com/yourusername/yourusername.github.io`
2. Click **Settings** (gear icon)
3. In the left sidebar, click **Pages**
4. Under "Source", select:
   - Branch: `main` (or `master`)
   - Folder: `/ (root)`
5. Click **Save**

GitHub will start building your site. Wait 1-2 minutes.

## Step 5: Verify Deployment

1. Visit: `https://yourusername.github.io`
2. Your blog should be live!

If you see a 404, wait a few more minutes and refresh.

## Troubleshooting

### Site not showing

1. Check GitHub Pages status:
   - Go to Settings > Pages
   - Look for any error messages

2. Verify `_config.yml`:
   ```yaml
   url: "https://yourusername.github.io"
   baseurl: ""
   ```

3. Check build logs:
   - Go to Settings > Pages
   - Scroll down to see deployment history
   - Click on the deployment to see logs

### Custom domain issues

If using a custom domain:
1. Update `url` in `_config.yml`
2. Create a `CNAME` file in repo root with your domain
3. Configure DNS settings with your registrar

## Updating Your Blog

After deployment, updating is simple:

```bash
# Make changes to your blog (add posts, edit content, etc.)
git add .
git commit -m "Add new blog post about [topic]"
git push origin main
```

GitHub automatically rebuilds and deploys within 1-2 minutes.

## Monitoring Deployments

Check deployment status:
1. Go to your repository
2. Click the **⚡** icon (latest deployment) at the right
3. Click **Deployments** to see history
4. Click any deployment to see details

## Workflow: Adding Content

### Adding a Blog Post

1. Create file: `_posts/YYYY-MM-DD-title.md`
2. Add frontmatter and content
3. Commit and push:
   ```bash
   git add _posts/YYYY-MM-DD-title.md
   git commit -m "Add blog post: [title]"
   git push origin main
   ```

### Adding a Portfolio Item

1. Create file: `_portfolio/XX-project-name.md`
2. Add frontmatter and content
3. Commit and push:
   ```bash
   git add _portfolio/XX-project-name.md
   git commit -m "Add portfolio item: [project]"
   git push origin main
   ```

### Updating Pages

1. Edit files directly (about.md, services.md, etc.)
2. Commit and push:
   ```bash
   git add .
   git commit -m "Update [page name]"
   git push origin main
   ```

## Performance Tips

1. Optimize images before uploading
2. Use relative URLs for internal links
3. Keep posts under 5000 words for better performance
4. Use code snippets instead of full files

## Security Notes

- **Never** commit sensitive information (API keys, secrets)
- Keep `_config.yml` values appropriate for public viewing
- Use environment variables for sensitive data (GitHub Secrets)

## Custom Domain Setup

To use your own domain (e.g., myblog.com):

1. Update `_config.yml`:
   ```yaml
   url: "https://myblog.com"
   ```

2. Create a `CNAME` file in the repository root with:
   ```
   myblog.com
   ```

3. Configure DNS with your domain registrar:
   - A records pointing to GitHub's servers
   - Refer to [GitHub Docs](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site) for latest IPs

4. In GitHub Pages settings, verify custom domain

## Support

For issues:
- Check [GitHub Pages Documentation](https://docs.github.com/en/pages)
- Review [Jekyll Documentation](https://jekyllrb.com/docs/)
- See GitHub Pages build logs for errors

---

**Your blog is ready to deploy! 🚀**
