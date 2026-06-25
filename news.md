---
layout: page
title: News
permalink: /news/
---

<div class="posts">
  {% for post in site.tags.news %}
  <article class="post">
    <h1><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></h1>
    <div class="entry">{{ post.content | strip_html | truncatewords:40}}</div>
    <a href="{{ site.baseurl }}{{ post.url }}" class="read-more">더 읽기</a>
  </article>
  {% endfor %}
</div>
