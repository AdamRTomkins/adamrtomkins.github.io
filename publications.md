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
    <h1 class="post-title">request for comments</h1>
</header>

<ul class="post-list">
{% for rfc in site.rfcs reversed %}
    <li>
        <h2><a class="poem-title" href="{{ rfc.url | prepend: site.baseurl }}">{{ rfc.title }}</a></h2>
        <p class="post-meta">{{ rfc.date | date: '%B %-d, %Y — %H:%M' }}</p>
      </li>
{% endfor %}
</ul>
