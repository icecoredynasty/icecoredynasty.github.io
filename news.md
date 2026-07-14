---
layout: page
title: ""
hide_title: true
permalink: /news/
---
<section class="homepage-intro">

<h1>League News</h1>

<p class="intro">
Official announcements, league updates, keeper deadlines, trade news,
draft information and everything happening in IceCore Dynasty.
</p>

</div>

<div class="news-grid">

{% for post in site.posts %}

<div class="news-card">

<a href="{{ post.url }}">

{% if post.image %}
<img src="{{ post.image.path }}" alt="{{ post.title }}">
{% endif %}

<h3>{{ post.title }}</h3>

<p>{{ post.excerpt | strip_html | truncate:140 }}</p>

</a>

</div>

{% endfor %}

</div>
