---
layout: index
---

<ul class="posts">
  {% for post in site.posts %}
  <li>
    <div class="date">{{ post.date | date_to_string }} </div>
    <a href="{{ post.url }}/#content">{{ post.title }}</a>
  </li>
  {% endfor %}
</ul>
