---
layout: post.njk
title: "Getting Started with Eleventy: A Beginner's Guide"
date: 2024-01-20
description: "Learn how I set up this blog using Eleventy, from installation to deployment on GitHub Pages."
tags: ["posts", "tutorial", "eleventy", "static-site-generator"]
---

# Getting Started with Eleventy

In this post, I'll walk through how I built this blog using [Eleventy](https://www.11ty.dev/), a fantastic static site generator that's both powerful and beginner-friendly.

## Why Eleventy?

After researching various static site generators, I chose Eleventy for several reasons:

- **Simple to get started** - minimal configuration required
- **Flexible** - supports multiple template languages
- **Fast builds** - generates sites quickly
- **Great documentation** - excellent learning resources
- **Active community** - helpful support and plugins

## Setting Up the Project

Here's a quick overview of the setup process:

### 1. Initialize the Project

```bash
npm init -y
npm install --save-dev @11ty/eleventy
```

### 2. Create Basic Structure

```
src/
├── _layouts/          # Template files
├── _includes/         # Reusable components
├── posts/            # Blog posts
├── css/              # Stylesheets
└── index.njk         # Homepage
```

### 3. Configure Eleventy

The `.eleventy.js` configuration file tells Eleventy how to process your site:

```javascript
module.exports = function(eleventyConfig) {
  // Copy static assets
  eleventyConfig.addPassthroughCopy("src/css");
  
  // Set up input/output directories
  return {
    dir: {
      input: "src",
      output: "_site"
    }
  };
};
```

## Key Features I Implemented

### Date Formatting
Created custom filters for displaying dates in a readable format.

### Post Collections
Set up automatic collection of blog posts with proper sorting.

### Responsive Design
Used CSS Grid and Flexbox for a mobile-friendly layout.

## Deployment with GitHub Pages

The final step was setting up automated deployment using GitHub Actions, which I'll cover in detail in my next post!

## Resources

- [Eleventy Documentation](https://www.11ty.dev/docs/)
- [Eleventy Base Blog](https://github.com/11ty/eleventy-base-blog) - Great starter template
- [11ty Rocks](https://11ty.rocks/) - Excellent tutorials and resources

---

*This post is part of my learning journey in the TU856-4 course.*