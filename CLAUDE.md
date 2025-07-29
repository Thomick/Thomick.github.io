# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Development Commands

### Local Development
To run the site locally using Docker:
```bash
docker build -t jekyll-site .
docker run -p 4000:4000 --rm -v $(pwd):/usr/src/app jekyll-site
```

Alternative using docker-compose:
```bash
docker-compose up
```

### JavaScript/Asset Management
Build minified JavaScript:
```bash
npm run build:js
```

Watch for JavaScript changes:
```bash
npm run watch:js
```

### Bundle Management
Install Ruby dependencies:
```bash
bundle install
```

Serve Jekyll site locally (alternative to Docker):
```bash
bundle exec jekyll serve --host 0.0.0.0 --watch
```

## Architecture Overview

This is a Jekyll-based personal academic website using the Academic Pages template (version 0.8.1.1), which is a fork of the Minimal Mistakes theme. The site is hosted on GitHub Pages and showcases academic work, publications, and projects.

### Key Structure
- **Jekyll Collections**: The site uses Jekyll collections for different content types:
  - `_publications/`: Academic publications with metadata
  - `_pages/`: Main site pages (about, CV, projects, etc.)
  - `_talks/`: Conference talks and presentations
  - `_teaching/`: Teaching materials and courses
  - `_portfolio/`: Project portfolio items

- **Content Organization**: 
  - Main content is in Markdown files with YAML front matter
  - Static assets (PDFs, images) stored in `/files/` and `/images/`
  - Modular SASS structure in `/_sass/` with organized subdirectories:
    - `layout/`: Page layout styles
    - `theme/`: Theme-specific styles (default and dark themes)
    - `include/`: Mixins and utilities
  - Site configuration in `_config.yml`

- **Theme Support**: Built-in dark/light theme support
  - Set `site_theme: "dark"` in `_config.yml` for dark mode
  - Themes defined in `_sass/theme/_dark.scss` and `_sass/theme/_default.scss`

### Template Features
- **Publication Categories**: Support for different publication types (books, manuscripts, conferences)
- **CV Generation**: Both Markdown and JSON-based CV layouts available
- **Social Media Integration**: Built-in support for academic and social platforms including Bluesky
- **Responsive Design**: Mobile-friendly layouts
- **Enhanced Navigation**: Configurable header navigation via `_data/navigation.yml`

### Custom Content
- **Interactive Elements**: Custom slime visualization at `_pages/slime.html`
- **Personal Academic Files**: Research papers, CV, and presentation materials in `/files/`
- **Custom About Page**: Personalized biography and research overview

### Deployment
- GitHub Pages compatible
- Uses `github-pages` gem for dependency management
- Automated builds triggered by pushes to master branch
- Site available at https://thomick.github.io/

## Navigation Configuration
Navigation items can be enabled/disabled in `_data/navigation.yml`. Currently disabled items are commented out and can be re-enabled by uncommenting:
- Talks
- Teaching
- Portfolio
- Guide

## File Locations
- Configuration: `_config.yml`
- Main pages: `_pages/`
- Publications: `_publications/`
- Static files: `files/`, `images/`
- Styles: `_sass/` (organized by layout/, theme/, include/)
- JavaScript: `assets/js/`
- Navigation: `_data/navigation.yml`