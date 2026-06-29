# Into The Wild — Hugo Adventure Blog

A personal adventure blog built with [Hugo](https://gohugo.io/) and the [LoveIt theme](https://github.com/dillonzq/LoveIt), hosted free on GitHub Pages.

---

## 🚀 First-Time Setup

### 1. Use this repo on GitHub
- Create a new repo named `yourusername.github.io`
- Push this folder to it

### 2. Add LoveIt theme
```bash
git submodule add https://github.com/dillonzq/LoveIt.git themes/LoveIt
```

### 3. Update hugo.toml
- Replace `yourusername` with your actual GitHub username
- Update the `baseURL` to `https://yourusername.github.io/`
- Fill in your name, social links, avatar, etc.

### 4. Enable GitHub Pages
- Go to your repo → **Settings** → **Pages**
- Set Source to **GitHub Actions**
- Push to `main` — your site deploys automatically ✅

---

## ✍️ Writing a New Post

```bash
hugo new posts/my-adventure.md
```

This creates a file in `content/posts/` from the archetype template.

Edit the front matter at the top:
```yaml
---
title: "My Adventure"
date: 2024-09-01
draft: false          # ← change to false when ready to publish
tags: ["hiking", "alps"]
categories: ["Mountains"]
featuredImage: "/images/my-photo.jpg"
---
```

Then write your post in Markdown below the `---`.

### Adding images
Drop photos into `static/images/` and reference them as `/images/yourphoto.jpg`.

---

## 👀 Preview Locally

```bash
# Install Hugo (extended version)
# macOS:
brew install hugo

# Windows:
winget install Hugo.Hugo.Extended

# Run local server
hugo server -D
```

Open http://localhost:1313 in your browser.

---

## 📁 Project Structure

```
adventure-blog/
├── .github/workflows/
│   └── deploy.yml          # Auto-deploys on every push to main
├── content/
│   ├── posts/              # Your blog posts go here
│   └── about.md            # About page
├── static/
│   └── images/             # Photos and images
├── themes/
│   └── LoveIt/             # Theme (added as git submodule)
├── archetypes/
│   └── posts.md            # Template for new posts
└── hugo.toml               # Site configuration
```

---

## 🌐 Custom Domain (optional)

1. Buy a domain (Namecheap, Cloudflare, etc.)
2. Add a file called `CNAME` in the `static/` folder containing just your domain:
   ```
   www.yourdomain.com
   ```
3. Point your domain's DNS to GitHub Pages (follow [GitHub's guide](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site))

---

Happy adventuring! 🏔️
