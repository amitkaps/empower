---
layout: default
---

<div>
  {% for post in site.posts %}
      <a href="{{ post.url }}"><h2>{{ post.title }}</h2></a>
      {{ post.content | truncatewords:50 | strip_html }}
      <br/>
      <br/>
  {% endfor %}
</div>