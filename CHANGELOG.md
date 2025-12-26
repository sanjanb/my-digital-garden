# Changelog

All notable changes to this digital garden will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/).

## [2.0.0] - 2025-12-26

### 🎉 Major Overhaul - Feature-Complete Digital Garden

This update transforms the template into a fully-featured, production-ready digital garden.

### Added

#### Phase 1: Content Foundation

- **Taxonomy System**: Three comprehensive index pages
  - Programming Index (`index-programming.md`)
  - Systems Thinking Index (`index-systems-thinking.md`)
  - Personal Development Index (`index-personal-development.md`)
- **Updated About Page**: Personalized structure with clear navigation guidance
- **Enhanced Note**: Transformed `your-first-note.md` into "How This Garden Works"
- **Tags**: Added tag support to existing core notes

#### Phase 2: Feature Enhancements

- **Full-Text Search** (`/search`)
  - Client-side JavaScript search
  - Search across titles, content, and tags
  - Highlighted search results
  - Search data JSON endpoint
- **Tagging System** (`/tags`)
  - Tag display on note pages
  - Browseable tag index
  - Tag-based filtering
- **Dark Mode**
  - CSS custom properties for theming
  - Persistent theme selection (localStorage)
  - Smooth transitions
  - Theme toggle in navigation
- **RSS Feed**
  - Jekyll Feed plugin integration
  - Automatic feed generation
  - Proper collection support

#### Phase 3: Publishing & Sharing

- **Start Here Guide** (`/start`)
  - Comprehensive onboarding
  - Navigation tips
  - Reading paths
  - Philosophy explanation
- **Garden Network Page** (`/network`)
  - Links to other digital gardens
  - Community resources
  - Tool recommendations
- **Subscribe Page** (`/subscribe`)
  - RSS feed promotion
  - Newsletter signup form
  - Social media links
- **Roadmap Page** (`/roadmap`)
  - Development timeline
  - Feature tracking
  - Growth metrics
  - Future plans
- **Quick Reference** (`/reference`)
  - Keyboard shortcuts
  - Tag conventions
  - Link types
  - Power user tips

### Enhanced

#### Navigation

- Reorganized main navigation menu
- Added Search, Tags, and Start links
- Improved navigation structure
- Added dark mode toggle button

#### SEO & Metadata

- Comprehensive Open Graph tags
- Twitter Card support
- Meta descriptions
- Author and keyword meta tags
- RSS feed link in head
- Canonical URLs
- Article published/modified times

#### Styling

- CSS custom properties for theming
- Dark mode color palette
- Improved contrast ratios
- Better mobile responsiveness
- Smoother transitions

#### Footer

- Multi-column layout
- Quick links to important pages
- Social/source links
- Year copyright (dynamic)

### Changed

- **Config**: Added description, author, url fields
- **Gemfile**: Added jekyll-feed plugin
- **Note Layout**: Added tag display, removed placeholder text
- **Navigation**: Completely restructured menu
- **Footer**: Complete redesign with better organization

### Documentation

- **README.md**: Comprehensive rewrite with:
  - Quick start guide
  - Customization instructions
  - Deployment guides
  - Project structure overview
- **SETUP-CHECKLIST.md**: Step-by-step personalization guide
- **Changelog**: This file

### Files Added

```
_notes/
  ├── index-programming.md
  ├── index-systems-thinking.md
  └── index-personal-development.md
_pages/
  ├── start.md
  ├── search.md
  ├── tags.md
  ├── subscribe.md
  ├── network.md
  ├── roadmap.md
  └── reference.md
search-data.json
SETUP-CHECKLIST.md
```

### Technical Improvements

- Modular SCSS with CSS variables
- Better accessibility (aria-labels)
- Improved semantic HTML
- Performance optimizations
- No external dependencies for core features

---

## [1.0.0] - Initial Template

### Original Features

- Bidirectional linking with Roam-style syntax
- Interactive graph visualization
- Link previews on hover
- Responsive design
- Jekyll 4.4 base
- Custom plugins for backlinks
- Basic styling

### Template Notes

- Based on Maxime Vaillancourt's Digital Garden template
- Example notes included
- Basic navigation structure

---

## Future Versions

See [Roadmap](/roadmap) for planned features in upcoming releases.

### Planned for 2.1.0

- [ ] Note templates system
- [ ] Changelog automation
- [ ] Contribution stats visualization
- [ ] Enhanced graph filtering

### Backlog

- Interactive graph filtering by tags
- Note maturity indicators (seedling/budding/evergreen)
- Reading progress tracking
- Export functionality
- Comment system (webmentions)

---

## Migration Notes

If updating from the original template:

1. **Backup your content**: Copy all your notes from `_notes/`
2. **Pull latest changes**: Get all new files
3. **Restore your notes**: Add back your content
4. **Update config**: Set your personal details in `_config.yml`
5. **Run bundle install**: Install new dependencies (jekyll-feed)
6. **Test locally**: Verify everything works
7. **Customize**: Follow SETUP-CHECKLIST.md

---

**Last Updated**: December 26, 2025
