---
layout: page
title: Vyhledávání v Techblogu
permalink: /search.html
---

<div id="search-container">
    <input type="text" id="search-input" placeholder="Hledej v Techblogu...">
    <ul id="results-container"></ul>
</div>

<script src="{{ site.baseurl }}/assets/simple-jekyll-search.min.js" type="text/javascript"></script>

<script>
    SimpleJekyllSearch({
    searchInput: document.getElementById('search-input'),
    resultsContainer: document.getElementById('results-container'),
    searchResultTemplate: '<div style="text-align: left !important;"><a href="{url}"><h1 style="text-align:left !important;">{title}</h1></a><span style="text-align:left !important;">{{ post.date | date: "%-e. %-m. %Y" }}</span></div>',
    json: '{{ site.baseurl }}/search.json'
    });
</script>