---
layout: default
title: Articles
---

{% for post in site.posts %}
  <article>
    <a href="{{ post.url }}">{{ post.title }}</a>
  </article>
{% endfor %}

