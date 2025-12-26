---
layout: page
title: Tags
permalink: /tags
---

# Browse by Tag

Explore notes organized by topic and theme.

<div style="margin: 2em 0;">
{% assign tags = site.notes | map: 'tags' | compact | join: ',' | split: ',' | uniq | sort %}

{% for tag in tags %}
  {% assign tag_notes = site.notes | where_exp: "note", "note.tags contains tag" %}
  <div style="margin-bottom: 2em;">
    <h3 id="{{ tag | slugify }}" style="border-bottom: 2px solid #dee2e6; padding-bottom: 0.5em; margin-bottom: 1em;">
      #{{ tag }} <span style="font-size: 0.7em; color: #666;">({{ tag_notes.size }})</span>
    </h3>
    <div style="display: grid; grid-gap: 1em; margin-left: 1em;">
      {% for note in tag_notes %}
      <div style="padding: 0.75em 1em; background: #f8f9fa; border-left: 3px solid #dee2e6; border-radius: 3px;">
        <a class="internal-link" href="{{ site.baseurl }}{{ note.url }}" style="font-weight: 500;">{{ note.title }}</a>
        <div style="font-size: 0.85em; color: #666; margin-top: 0.3em;">
          {{ note.excerpt | strip_html | truncatewords: 20 }}
        </div>
      </div>
      {% endfor %}
    </div>
  </div>
{% endfor %}
</div>

<style>
  .wrapper {
    max-width: 46em;
  }
</style>
