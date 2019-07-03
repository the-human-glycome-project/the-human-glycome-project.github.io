---
layout: page
title: News
permalink: /news/
---

<ul class="post-list">
  {% for post in site.posts %}
    <li>
      <span class="post-meta">{{ post.date | date_to_string }}, {{ post.author }}</span>
      <h3><a class="post-link" href="{{ post.url }}">{{ post.title }}</a></h3>
      {{ post.content }}
    </li>
  {% endfor %}
