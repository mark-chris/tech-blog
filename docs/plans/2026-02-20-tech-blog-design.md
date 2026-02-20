# Tech Blog Design

## Overview

A personal tech blog focused on appsec, prodsec, devsecops, and AI security. Built with Hugo using the Terminal theme, hosted on GitHub Pages with GitHub Actions CI/CD. Custom domain to be added later.

## Content Sections

- **Blog posts** (`content/posts/`): Articles organized by date with flat tags (e.g., `appsec`, `ai-security`, `devsecops`, `prodsec`, `llm-security`)
- **Projects** (`content/projects/`): Portfolio of personal projects, each as a markdown file with title, description, URL, and tags
- **About** (`content/about.md`): Static bio/about page

## Theme Installation

Hugo Module (not git submodule). Configured via `go.mod` and the `[module]` block in `config.toml`. No `theme` parameter needed.

## Site Structure

```
tech-blog/
├── config.toml
├── content/
│   ├── posts/
│   ├── projects/
│   └── about.md
├── layouts/
│   └── projects/
│       └── list.html
├── static/
├── .github/
│   └── workflows/
│       └── deploy.yml
└── go.mod / go.sum
```

## Navigation

Three top-level menu items: Blog, Projects, About.

## Projects Section

Custom `layouts/projects/list.html` overriding the theme's default list template since Terminal only supports one content type natively.

## Taxonomy

Tags only. No categories or series.

## Deployment

GitHub Actions workflow triggered on push to `main`:
1. Install Hugo Extended + Go
2. Build with `hugo --minify`
3. Deploy to GitHub Pages

## Starter Content

- Example "Hello World" blog post
- Placeholder About page
- Placeholder Projects page with one example project

## Custom Domain

Deferred. Will be configured later via GitHub Pages settings and a CNAME file.
