

---
layout: default
title: Blog Archive
---

{% for tag in site.tags %}
  <h2>{{ tag[0] }}</h2>
  {% for post in tag[1] %}
    <div class="post-preview">
      <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
      <img src="{{ post.image }}" alt="{{ post.title }}" style="max-width:100%; height:auto;">
      <p>{{ post.excerpt | truncate: 150, "" }}</p>
    </div>
  {% endfor %}
{% endfor %}
