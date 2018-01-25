---
layout: page
permalink: /publications/
title: publications and presentations
description: A collection of my academic publications and presentations.
---

<img class="col one right" src="/img/publications.jpg">

<ul class="post-list">
{% for publication in site.publications reversed %}
    <li>
        <h2><a class="poem-title" href="{{ publication.url | prepend: site.baseurl }}">{{ publication.title }}</a></h2>
        <p class="post-meta">{{ publication.date | date: '%B %-d, %Y — %H:%M' }}</p>
      </li>
{% endfor %}
</ul>

