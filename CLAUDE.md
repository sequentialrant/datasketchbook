# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is "The Data Sketchbook" - a Quarto-based website for technical blogs and talks on machine learning and data science. The site features reproductions of data visualizations and insights from data visualization books.

## Architecture

- **Quarto Website**: The site uses Quarto's website project type with automatic execution freezing
- **Content Structure**: Blog posts are stored in `posts/` directory, each in its own folder with `index.qmd` and an `images/` subdirectory
- **Styling**: Uses Bootstrap themes (Litera for light mode, Darkly for dark mode) with custom SCSS overrides in `custom.scss`
- **Build Output**: Generated site files are placed in `_site/` directory

## Key Files

- `_quarto.yml`: Main configuration file defining website structure, themes, and build settings
- `index.qmd`: Homepage with blog listing configuration using Quarto's listing feature
- `custom.scss`: Custom styling that imports Atkinson Hyperlegible and Fira Code fonts
- `posts/*/index.qmd`: Individual blog post files with YAML frontmatter

## Common Commands

### Building and Serving
```bash
quarto preview              # Start development server with live reload
quarto render               # Build the entire website to _site/
quarto publish              # Publish to configured hosting service
```

### Content Management
```bash
quarto create-project blog  # Create new blog post structure
```

## Development Notes

- Blog posts use YAML frontmatter with `title`, `author`, `date`, and `toc` fields
- Images should be placed in `posts/{post-name}/images/` directory
- The site uses automatic execution freezing (`freeze: auto`) to cache computational results
- Custom fonts (Atkinson Hyperlegible for body text, Fira Code for code) are loaded via Google Fonts
- Google Analytics is configured with ID 'G-4BTEYBVWPE'

## Content Guidelines

- Posts focus on data visualization, machine learning, and data science topics
- Include proper attribution for data sources
- Use relative paths for images within post directories
- Follow the established naming convention for post directories (lowercase with hyphens)