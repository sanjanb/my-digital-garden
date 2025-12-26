# Writing Guide for Your Digital Garden 🌱

Quick reference for creating and maintaining notes in your digital garden.

## Creating a New Note

### 1. File Location

Create a new `.md` file in `_notes/`:

```bash
_notes/my-new-note.md
```

For organized topics, use subdirectories:

```bash
_notes/programming/design-patterns.md
_notes/books/atomic-habits.md
```

### 2. Basic Template

```markdown
---
title: Your Note Title
tags: [tag1, tag2, tag3]
---

# Your Note Title

First paragraph should be a clear introduction or summary.

## Main Content

Your ideas, insights, and connections go here.

Link to related notes with [[Other Note Title]].

## Related Concepts

- [[Related Note 1]]
- [[Related Note 2]]
```

### 3. Frontmatter Fields

**Required:**

```yaml
---
title: Your Note Title
---
```

**Recommended:**

```yaml
---
title: Your Note Title
tags: [topic, category, type]
---
```

**Optional:**

```yaml
---
title: Your Note Title
tags: [topic, category]
excerpt: Custom excerpt for previews
image: /assets/images/cover.jpg
---
```

## Linking Strategy

### Internal Links (Preferred)

```markdown
[[Note Title]] # Links by title
[[filename]] # Links by filename
[[Note Title|custom text]] # Custom link text
```

### Regular Markdown Links

```markdown
[External Site](https://example.com)
[Internal Page](/about)
```

### Link Best Practices

- ✅ Link liberally - connections create value
- ✅ Link in both directions when relevant
- ✅ Use descriptive link text
- ❌ Don't link the same note multiple times in one paragraph
- ❌ Don't create circular link chains

## Tagging System

### Tag Categories

**By Domain:**

- `programming` `systems` `personal-growth` `career` `learning`

**By Type:**

- `index` `meta` `guide` `framework` `pattern` `concept` `tool`

**By Status:**

- `active` `exploration` `reference` `draft` `start-here`

**By Format:**

- `essay` `list` `question` `definition` `example`

### Tagging Best Practices

- Use 2-5 tags per note
- Be consistent with tag names (use existing tags when possible)
- Combine domain + type tags
- Review `/tags` page periodically to consolidate similar tags

## Note Development Stages

Mark maturity in your content (optional):

**🌱 Seedling** - New notes, rough ideas

```markdown
> 🌱 Seedling - This is a rough note, still developing
```

**🌿 Budding** - Developing with connections

```markdown
> 🌿 Budding - Actively developing this concept
```

**🌳 Evergreen** - Well-established, regularly updated

```markdown
> 🌳 Evergreen - This note is well-developed and regularly updated
```

## Writing Tips

### Start Small

- Write a single sentence
- Add another when inspiration strikes
- Let notes grow organically

### Embrace Incompleteness

- Publish rough drafts
- Mark areas for expansion: `[TODO: expand this]`
- Return and refine over time

### Build Connections

- Reference at least one other note
- Ask: "What does this relate to?"
- Create bidirectional links

### Write for Future You

- Explain concepts clearly
- Include examples
- Link to sources

## Content Patterns

### Concept Note

```markdown
---
title: Concept Name
tags: [concept, domain]
---

# Concept Name

## Definition

Clear, concise definition.

## Key Ideas

- Main point 1
- Main point 2

## Examples

Real-world applications.

## Related

- [[Similar Concept]]
- [[Contrasting Concept]]
```

### Index/Hub Note

```markdown
---
title: Topic Index
tags: [index, domain]
---

# Topic Index

Overview of this topic area.

## Core Concepts

- [[Concept 1]]
- [[Concept 2]]

## Related Areas

- [[Related Index]]

## Current Questions

- What are we exploring?
```

### Question Note

```markdown
---
title: How does X work?
tags: [question, exploration]
---

# How does X work?

## Initial Thoughts

Current understanding.

## Investigations

- [[Research 1]]
- [[Research 2]]

## Emerging Answers

Partial insights.

## Related Questions

- [[Question 2]]
```

### Book/Resource Note

```markdown
---
title: Book Title - Author
tags: [book, topic]
---

# Book Title by Author

## Key Takeaways

- Insight 1
- Insight 2

## Memorable Quotes

> "Quote here"

## Connections

- Relates to [[Concept]]
- Challenges [[Another Concept]]

## My Thoughts

Personal reflections.
```

## Maintenance Tasks

### Weekly

- [ ] Add 1-2 new notes
- [ ] Update 1 existing note
- [ ] Check for broken internal links
- [ ] Review and respond to any feedback

### Monthly

- [ ] Review tag usage on `/tags` page
- [ ] Update index pages with new notes
- [ ] Strengthen weak connections
- [ ] Archive or delete stale drafts

### Quarterly

- [ ] Major reorganization if needed
- [ ] Update roadmap
- [ ] Review growth metrics
- [ ] Celebrate progress!

## Formatting Tips

### Headings

```markdown
# Note Title (h1 - use once)

## Section (h2 - main sections)

### Subsection (h3 - details)
```

### Emphasis

```markdown
**bold** for important terms
_italic_ for emphasis
`code` for technical terms
```

### Lists

```markdown
- Unordered list
- For collections

1. Ordered list
2. For sequences
```

### Quotes

```markdown
> Blockquote for
> referenced content
```

### Code Blocks

````markdown
```language
code here
```
````

### Callouts (Manual)

```markdown
> 💡 **Tip**: Helpful advice here

> ⚠️ **Warning**: Important caveat

> 📝 **Note**: Additional context
```

## Publishing Checklist

Before publishing a new note:

- [ ] Title is clear and descriptive
- [ ] Front matter includes relevant tags
- [ ] At least one internal link to another note
- [ ] Content is readable (spell-check)
- [ ] Examples or explanations provided
- [ ] Related notes updated with backlinks
- [ ] Added to relevant index if applicable

## Common Mistakes to Avoid

❌ **Over-organizing too early** - Let structure emerge
❌ **Waiting for "perfect" notes** - Ship rough drafts
❌ **Orphan notes** - Always connect to something
❌ **Too many tags** - Keep focused (2-5 max)
❌ **No internal links** - Connections create value
❌ **Inconsistent naming** - Check existing notes first

## Quick Commands

### Test Locally

```bash
bundle exec jekyll serve
```

### Build Site

```bash
bundle exec jekyll build
```

### New Note Quick Start

```bash
# Create from template
touch _notes/new-note.md
```

Then add frontmatter and start writing!

---

## Need Inspiration?

- Browse `/random` for serendipity
- Review `/current-investigations` for active topics
- Check other gardens in `/network`
- Read your own older notes - they spark new ideas

---

**Happy gardening! 🌱** Remember: The best note is the one you actually write.
