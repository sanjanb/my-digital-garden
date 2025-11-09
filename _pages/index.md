---
layout: page
title: Home
id: home
permalink: /
---

# The Archive

<p style="padding: 2em 1.5em; background: #f8f9fa; border-left: 3px solid #dee2e6; font-style: italic;">
  "The mind, once expanded by a new idea, never returns to its original dimensions." — Begin with <span style="font-weight: bold">[[The Threshold]]</span> or follow the recent traces below.
</p>

This repository contains fragments of understanding, half-formed theories, and connections that emerge in the spaces between disciplines. Each entry is both a destination and a departure point.

What you encounter here resists simple categorization. Some thoughts are fully formed; others remain deliberately incomplete, waiting for the right connection to give them meaning.

**Recent additions to the archive**

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
