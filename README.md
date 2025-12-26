# Sanjan's Digital Garden 🌱

A personal knowledge management system built with Jekyll, featuring bidirectional linking, graph visualization, and evolving notes.

**Live Site**: [Your URL Here]

## What is This?

This is a **digital garden**—a collection of interconnected notes that grow and evolve over time. Unlike a traditional blog with finished, chronological posts, a garden embraces:

- 🌱 **Growth over perfection** - Notes improve incrementally
- 🔗 **Connections over isolation** - Ideas link to create insights
- 🚧 **Process over product** - Works-in-progress have value
- 🧪 **Exploration over certainty** - Questions drive learning

## Features

### Core Functionality

- ✅ **Bidirectional Links** - Roam-style `[[wiki links]]` with automatic backlinks
- ✅ **Graph Visualization** - Interactive network of connected notes
- ✅ **Link Previews** - Hover to preview notes without navigating
- ✅ **Responsive Design** - Works on all devices

### Enhanced Features

- ✅ **Full-Text Search** - Find content across all notes
- ✅ **Tagging System** - Organize and browse by topic
- ✅ **Dark Mode** - Toggle between light/dark themes
- ✅ **RSS Feed** - Subscribe to updates
- ✅ **SEO Optimized** - Meta tags, Open Graph, Twitter Cards

## Quick Start

### Prerequisites

- Ruby 3.x
- Bundler
- Jekyll 4.4+

### Installation

1. **Clone the repository**

   ```bash
   git clone https://github.com/yourusername/my-digital-garden.git
   cd my-digital-garden
   ```

2. **Install dependencies**

   ```bash
   bundle install
   ```

3. **Run locally**

   ```bash
   bundle exec jekyll serve
   ```

4. **Open in browser**
   ```
   http://localhost:4000
   ```

## Customization

### 1. Update Site Configuration

Edit [`_config.yml`](_config.yml):

```yaml
title: Your Garden Name
description: Your garden description
author: Your Name
url: https://your-site-url.com
```

### 2. Personalize Content

- **About Page**: Edit [`_pages/about.md`](_pages/about.md)
- **Home Page**: Edit [`_pages/index.md`](_pages/index.md)
- **Start Guide**: Edit [`_pages/start.md`](_pages/start.md)

### 3. Add Your First Note

Create a new file in `_notes/`:

```markdown
---
title: My First Real Note
tags: [topic, category]
---

# My First Real Note

Content goes here with [[links to other notes]].
```

### 4. Update Social Links

Replace placeholders in:

- [`_pages/about.md`](_pages/about.md)
- [`_pages/subscribe.md`](_pages/subscribe.md)
- [`_pages/network.md`](_pages/network.md)
- [`_includes/head.html`](_includes/head.html) (Twitter handle)

## Project Structure

```
├── _config.yml           # Site configuration
├── _notes/               # Your notes (Markdown files)
│   ├── index-*.md       # Index/hub pages
│   └── *.md             # Individual notes
├── _pages/              # Static pages
│   ├── about.md
│   ├── start.md
│   ├── search.md
│   └── tags.md
├── _layouts/            # HTML templates
│   ├── default.html
│   ├── note.html
│   └── page.html
├── _includes/           # Reusable components
│   ├── head.html
│   ├── nav.html
│   └── footer.html
├── _plugins/            # Custom Jekyll plugins
│   └── bidirectional_links_generator.rb
├── _sass/               # Stylesheets
│   ├── _style.scss      # Main styles (with dark mode)
│   ├── _code.scss
│   └── _normalize.scss
└── assets/              # Static files
```

## Deployment

### Netlify (Recommended)

1. Push to GitHub
2. Connect repository to Netlify
3. Build settings:
   - **Build command**: `jekyll build`
   - **Publish directory**: `_site`
4. Deploy!

Configuration already set in [`netlify.toml`](netlify.toml).

### GitHub Pages

Note: GitHub Pages doesn't fully support custom plugins. The graph visualization requires the bidirectional links plugin. Options:

1. **Build locally** and push `_site/` to `gh-pages` branch
2. **Use GitHub Actions** to build with custom plugins
3. **Use Netlify instead** (recommended)

## Writing Notes

### Basic Syntax

```markdown
---
title: Note Title
tags: [tag1, tag2]
---

# Heading

Regular markdown content.

Link to other notes with [[Note Title]] or [[filename]].
```

### Linking

- `[[Note Title]]` - Links by title
- `[[filename]]` - Links by filename
- `[[Title|Custom Text]]` - Links with custom text

### Tags

Add tags in frontmatter:

```yaml
---
title: My Note
tags: [programming, systems-thinking, meta]
---
```

Browse all tags at `/tags`.

## Roadmap

See [Roadmap](https://your-site-url.com/roadmap) for planned features and development timeline.

### Recently Completed

- ✅ Tagging system
- ✅ Search functionality
- ✅ Dark mode
- ✅ RSS feed
- ✅ Enhanced SEO

### Next Up

- 🚧 Content expansion (10+ new notes)
- 🚧 Note templates
- 🚧 Changelog tracking
- 🚧 Related notes algorithm

## Resources

### Digital Gardening

- [The Garden and the Stream](https://hapgood.us/2015/10/17/the-garden-and-the-stream-a-technopastoral/) - Mike Caulfield
- [Digital Garden ToS](https://www.swyx.io/digital-garden-tos) - Shawn Wang
- [Garden History](https://maggieappleton.com/garden-history) - Maggie Appleton

### Jekyll Resources

- [Jekyll Documentation](https://jekyllrb.com/docs/)
- [Liquid Template Language](https://shopify.github.io/liquid/)
- [Jekyll Plugins](https://jekyllrb.com/docs/plugins/)

## Credits

- **Template**: Based on [Maxime Vaillancourt's Digital Garden](https://github.com/maximevaillancourt/digital-garden-jekyll-template)
- **Customizations**: Extended with search, tagging, dark mode, and enhanced features

## License

Source code: [MIT License](LICENSE)

Content: © [Year] [Your Name]

---

**Questions?** Open an issue or reach out at your.email@example.com

Happy gardening! 🌱
