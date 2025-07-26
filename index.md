---
layout: default
title: home
---

# {{ site.title }}

[home]({{ "/" | relative_url }}) &nbsp;&nbsp; [about]({{ "/about" | relative_url }}) &nbsp;&nbsp; [projects]({{ "/projects" | relative_url }})

---

{% for post in site.posts %}
- [{{ post.title }}]({{ post.url | relative_url }}) <small>{{ post.date | date: "%Y-%m-%d" }}</small>
{% endfor %}