---
layout: page
title: Home
id: home
permalink: /
---

# The Archive

<p style="padding: 2em 1.5em; background: #f8f9fa; border-left: 3px solid #dee2e6; font-style: italic;">
  "The mind, once expanded by a new idea, never returns to its original dimensions." — Begin with <span style="font-weight: bold">[[The Threshold]]</span>, explore <span style="font-weight: bold">[[Current Investigations]]</span>, or follow the recent traces below.
</p>

This repository contains fragments of understanding, half-formed theories, and connections that emerge in the spaces between disciplines. Each entry is both a destination and a departure point.

What you encounter here resists simple categorization. Some thoughts are fully formed; others remain deliberately incomplete, waiting for the right connection to give them meaning.

**Recent additions to the archive**

<div style="margin: 2em 0;">
{% assign recent_notes = site.notes | sort: "last_modified_at_timestamp" | reverse %}
{% for note in recent_notes limit: 8 %}
  <div style="margin-bottom: 1.5em; padding: 1em; background: #f8f9fa; border-left: 3px solid #dee2e6;">
    <div style="display: flex; justify-content: space-between; align-items: flex-start; margin-bottom: 0.5em;">
      <a class="internal-link" href="{{ site.baseurl }}{{ note.url }}" style="font-weight: 500; color: #333;">{{ note.title }}</a>
      <span style="font-size: 0.8em; color: #666;">{{ note.last_modified_at | date: "%m/%d" }}</span>
    </div>
    <div style="font-size: 0.85em; color: #666; line-height: 1.4;">
      {{ note.excerpt | strip_html | truncatewords: 15 }}
    </div>
  </div>
{% endfor %}
</div>

<style>
  .wrapper {
    max-width: 46em;
  }
</style>
