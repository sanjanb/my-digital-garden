---
title: Serendipity Engine
layout: page
permalink: /random
---

<script>
document.addEventListener('DOMContentLoaded', function() {
    // Get all notes from the graph data
    const notes = [
        '/welcome-to-my-garden',
        '/adaptive-patterns', 
        '/conceptual-frameworks',
        '/conceptual-migration',
        '/paradox-of-boundaries',
        '/programming-concepts',
        '/career-development',
        '/your-first-note',
        '/cats',
        '/consistency'
    ];
    
    // Pick a random note (excluding current page)
    const currentPath = window.location.pathname;
    const availableNotes = notes.filter(note => !currentPath.includes(note.substring(1)));
    const randomNote = availableNotes[Math.floor(Math.random() * availableNotes.length)];
    
    // Redirect to random note
    window.location.href = '{{ site.baseurl }}' + randomNote;
});
</script>

# Redirecting to a random note...

_If you're reading this, JavaScript might be disabled. Here are some starting points:_

- [[The Threshold]] — Entry point for new visitors
- [[Adaptive Patterns]] — Cross-domain principles
- [[The Paradox of Boundaries]] — Constraints as creative forces
- [[Conceptual Migration]] — Ideas moving between fields
