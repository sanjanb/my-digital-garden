---
layout: page
title: Search
permalink: /search
---

# Search

<div style="margin: 2em 0;">
  <input 
    type="text" 
    id="search-input" 
    placeholder="Search notes..." 
    style="width: 100%; padding: 0.75em 1em; font-size: 1em; border: 2px solid #dee2e6; border-radius: 4px; box-sizing: border-box;"
    autofocus
  />
</div>

<div id="search-results" style="margin-top: 2em;"></div>

<script>
(function() {
  const searchInput = document.getElementById('search-input');
  const searchResults = document.getElementById('search-results');
  let notesData = [];

  // Fetch all notes data
  fetch('{{ site.baseurl }}/search-data.json')
    .then(response => response.json())
    .then(data => {
      notesData = data;
    });

  // Simple search function
  function search(query) {
    if (!query || query.length < 2) {
      searchResults.innerHTML = '<p style="color: #666; font-style: italic;">Type at least 2 characters to search...</p>';
      return;
    }

    const lowerQuery = query.toLowerCase();
    const results = notesData.filter(note => {
      return note.title.toLowerCase().includes(lowerQuery) ||
             note.content.toLowerCase().includes(lowerQuery) ||
             (note.tags && note.tags.some(tag => tag.toLowerCase().includes(lowerQuery)));
    });

    if (results.length === 0) {
      searchResults.innerHTML = '<p style="color: #666; font-style: italic;">No results found for "' + query + '"</p>';
      return;
    }

    let html = '<div style="margin-bottom: 1em; color: #666;">Found ' + results.length + ' result' + (results.length !== 1 ? 's' : '') + '</div>';
    html += '<div style="display: grid; grid-gap: 1em;">';
    
    results.forEach(note => {
      const excerpt = getExcerpt(note.content, lowerQuery);
      html += `
        <div style="padding: 1em; background: #f8f9fa; border-left: 3px solid #dee2e6; border-radius: 3px;">
          <a class="internal-link" href="${note.url}" style="font-weight: 500; font-size: 1.1em;">${note.title}</a>
          ${note.tags ? '<div style="margin-top: 0.5em;">' + note.tags.map(tag => '<span style="display: inline-block; padding: 0.2em 0.5em; margin-right: 0.3em; background: #e9ecef; border-radius: 3px; font-size: 0.75em; color: #495057;">#' + tag + '</span>').join('') + '</div>' : ''}
          <div style="font-size: 0.85em; color: #666; margin-top: 0.5em; line-height: 1.4;">
            ${excerpt}
          </div>
        </div>
      `;
    });
    
    html += '</div>';
    searchResults.innerHTML = html;
  }

  function getExcerpt(content, query) {
    const index = content.toLowerCase().indexOf(query);
    if (index === -1) {
      return content.substring(0, 150) + '...';
    }
    
    const start = Math.max(0, index - 50);
    const end = Math.min(content.length, index + query.length + 100);
    let excerpt = content.substring(start, end);
    
    if (start > 0) excerpt = '...' + excerpt;
    if (end < content.length) excerpt = excerpt + '...';
    
    // Highlight the search term
    const regex = new RegExp('(' + query + ')', 'gi');
    excerpt = excerpt.replace(regex, '<strong style="background: #fff3cd;">$1</strong>');
    
    return excerpt;
  }

  // Debounce search
  let timeout = null;
  searchInput.addEventListener('input', function() {
    clearTimeout(timeout);
    timeout = setTimeout(() => {
      search(this.value);
    }, 300);
  });

  // Initial message
  searchResults.innerHTML = '<p style="color: #666; font-style: italic;">Start typing to search across all notes...</p>';
})();
</script>

<style>
  .wrapper {
    max-width: 46em;
  }
</style>
