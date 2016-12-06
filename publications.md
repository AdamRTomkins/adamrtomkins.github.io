---
layout: page
permalink: /publications/
title: publications
description: A collection of my academic publications.
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

<header class="post-header">
    <h1 class="post-title">presentations</h1>
</header>

<ul class="post-list">
{% for presentation in site.presentations reversed %}
    <li>
        <h2><a class="poem-title" href="{{ presentation.url | prepend: site.baseurl }}">{{ presentation.title }}</a></h2>
        <p class="post-meta">{{ presentation.date | date: '%B %-d, %Y — %H:%M' }}</p>
      </li>
{% endfor %}
</ul>
