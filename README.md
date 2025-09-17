# TU856-4 College Blog

A static blog website built with [Eleventy (11ty)](https://www.11ty.dev/) and automatically deployed to GitHub Pages. This blog serves as a platform for documenting the learning journey throughout the TU856-4 course.

## 🚀 Features

- **Static Site Generation** with Eleventy
- **Responsive Design** - works on desktop and mobile
- **Blog Posts** with automatic collection and sorting
- **Markdown Support** for easy content creation
- **Automated Deployment** via GitHub Actions
- **GitHub Pages Hosting** - free and reliable

## 🛠️ Technologies Used

- [Eleventy (11ty)](https://www.11ty.dev/) - Static site generator
- [Nunjucks](https://mozilla.github.io/nunjucks/) - Template engine
- Markdown - Content format
- CSS3 - Styling
- GitHub Actions - CI/CD
- GitHub Pages - Hosting

## 📁 Project Structure

```
├── src/                    # Source files
│   ├── _layouts/          # Layout templates
│   │   ├── base.njk       # Base layout
│   │   └── post.njk       # Blog post layout
│   ├── posts/             # Blog posts (Markdown)
│   ├── css/               # Stylesheets
│   ├── index.njk          # Homepage
│   └── about.md           # About page
├── _site/                 # Generated site (ignored)
├── .eleventy.js           # Eleventy configuration
├── .github/workflows/     # GitHub Actions workflows
└── package.json           # Node.js dependencies
```

## 🏃‍♂️ Quick Start

### Prerequisites
- Node.js (version 18 or higher)
- npm

### Local Development

1. **Clone the repository**
   ```bash
   git clone https://github.com/cadrianmae/TU856-4-Website.git
   cd TU856-4-Website
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Start development server**
   ```bash
   npm run serve
   ```
   The site will be available at `http://localhost:8080`

4. **Build for production**
   ```bash
   npm run build
   ```

### Available Scripts

- `npm run build` - Build the site for production
- `npm run serve` - Start development server with hot reload
- `npm run debug` - Build with debug information
- `npm run clean` - Remove generated files

## ✍️ Writing Blog Posts

Create new blog posts in the `src/posts/` directory using Markdown format:

```markdown
---
layout: post.njk
title: "Your Post Title"
date: 2024-01-20
description: "Brief description of your post"
tags: ["posts", "tutorial", "your-tags"]
---

# Your Post Content

Write your post content here using Markdown syntax.
```

### Frontmatter Options

- `layout` - Template to use (typically `post.njk`)
- `title` - Post title
- `date` - Publication date (YYYY-MM-DD format)
- `description` - Brief description for homepage preview
- `tags` - Array of tags (always include "posts" for blog collection)

## 🚀 Deployment

The site automatically deploys to GitHub Pages when you push to the `main` branch:

1. **Push to main branch**
   ```bash
   git add .
   git commit -m "Add new blog post"
   git push origin main
   ```

2. **GitHub Actions will:**
   - Install dependencies
   - Build the site
   - Deploy to GitHub Pages

3. **Access your live site at:**
   `https://cadrianmae.github.io/TU856-4-Website/`

## ⚙️ Configuration

### Eleventy Configuration

The `.eleventy.js` file contains:
- Input/output directory settings
- Template engine configuration
- Date filters for blog posts
- Static file copying rules

### GitHub Actions

The deployment workflow (`.github/workflows/deploy.yml`) handles:
- Node.js setup
- Dependency installation
- Site building
- GitHub Pages deployment

## 📚 Course Integration

This blog is part of the TU856-4 course curriculum and serves to:
- Document learning progress
- Practice web development skills
- Share course-related insights
- Build a portfolio of academic work

## 🤝 Contributing

This is a personal academic blog, but suggestions and feedback are welcome:

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Submit a pull request

## 📝 License

This project is licensed under the ISC License - see the [LICENSE](LICENSE) file for details.

## 🎓 Academic Context

**Course:** TU856-4  
**Institution:** TU Dublin  
**Purpose:** Academic blog and web development practice

---

*Built with ❤️ using Eleventy and deployed on GitHub Pages*