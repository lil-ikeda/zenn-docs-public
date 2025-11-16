# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Overview

This is a Zenn documentation repository for managing and publishing technical articles and books on Zenn (zenn.dev), a Japanese technical publishing platform. Content is written in Markdown and managed locally using zenn-cli.

## Architecture

### Content Structure

- `articles/` - Zenn articles (tech blog posts)
  - Each article is a standalone Markdown file with frontmatter
  - Filename format: `{slug}.md` (e.g., `5b4ff343a60855.md`)
  - Frontmatter includes: title, emoji, type, topics, published status, published_at
- `books/` - Zenn books (long-form technical content organized into chapters)
  - Currently empty but follows Zenn's book structure conventions
  - Each book has a config file and chapter files
- `.keep` files maintain empty directory structure in git

### Frontmatter Format for Articles

```yaml
---
title: "Article title"
emoji: "⛳"
type: "tech"  # or "idea"
topics:
  - "topic1"
  - "topic2"
published: true  # or false
published_at: "2025-09-07 19:28"
---
```

## Development Commands

### Preview content locally
```bash
npx zenn preview
```
Starts a local development server to preview articles and books in the browser.

### Create new article
```bash
npx zenn new:article
```
Generates a new article file with a random slug in the `articles/` directory.

To create with a specific slug:
```bash
npx zenn new:article --slug my-article-slug
```

### Create new book
```bash
npx zenn new:book
```
Generates a new book directory structure in the `books/` directory.

To create with a specific slug:
```bash
npx zenn new:book --slug my-book-slug
```

### List content
```bash
npx zenn list:articles  # List all articles
npx zenn list:books     # List all books
```

### Check zenn-cli version
```bash
npx zenn --version
```

## Publishing Workflow

Content in this repository is published to Zenn by pushing to the connected GitHub repository. When files are committed and pushed:
- Articles with `published: true` are published/updated on Zenn
- Articles with `published: false` remain as drafts
- The `published_at` field controls the publication timestamp

## Important Notes

- All content must be in Japanese (this is a Japanese technical publishing platform)
- Article slugs are typically auto-generated random strings (e.g., `5b4ff343a60855`)
- Images should be stored in Zenn's CDN (uploaded through Zenn's web interface)
- The repository uses CommonJS module format (`"type": "commonjs"` in package.json)
- No build or compilation step is required - content is pure Markdown

## Reference Documentation

- [Zenn CLI Guide](https://zenn.dev/zenn/articles/zenn-cli-guide) - Official CLI usage guide (Japanese)
- [Zenn CLI Installation](https://zenn.dev/zenn/articles/install-zenn-cli) - Installation instructions (Japanese)
