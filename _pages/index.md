---
layout: page
title: Home
id: home
permalink: /
---

# Welcome to My Digital Garden! 🌱

<p style="padding: 3em 1em; background: #f5f7ff; border-radius: 4px;">
  Hi there! I'm <strong>Sanjan</strong>, and this is my personal knowledge garden. Start your exploration with <span style="font-weight: bold">[[Your first note]]</span> or browse through my recent thoughts below.
</p>

This is my space for **connecting ideas**, **documenting learnings**, and **sharing insights**. Unlike a traditional blog, this garden grows organically - ideas link to each other, creating a web of interconnected knowledge.

## 🎯 What's Growing Here

- **Learning notes** from books, courses, and experiences
- **Project documentation** and technical insights  
- **Personal reflections** and growth observations
- **Random discoveries** that spark curiosity

Feel free to wander around, follow the links, and discover unexpected connections!

<strong>Recently updated notes</strong>

<ul>
  {% assign recent_notes = site.notes | sort: "last_modified_at_timestamp" | reverse %}
  {% for note in recent_notes limit: 5 %}
    <li>
      {{ note.last_modified_at | date: "%Y-%m-%d" }} — <a class="internal-link" href="{{ site.baseurl }}{{ note.url }}">{{ note.title }}</a>
    </li>
  {% endfor %}
</ul>

<style>
  .wrapper {
    max-width: 46em;
  }
</style>
