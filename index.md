---
layout: default
---

{% for post in site.posts limit:2 %}
  <article>
    <h1>{{ post.title }}</h1>
    {{ post.excerpt }}
    <a href="{{ post.url }}">lire la suite</a>
  </article>
{% endfor %}


[Tout les articles](/articles)

