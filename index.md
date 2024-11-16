---
layout: page
title: Computing Bits and Bytes
---

<!-- <ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a> — {{ post.date | date: "%B %d, %Y" }}
      <p>{{ post.excerpt }}</p>
    </li>
  {% endfor %}
</ul> -->

<div class="latest-post">
  {% if site.posts.size > 0 %}
    {% assign latest_post = site.posts.first %}
    <article>
      <h2>{{ latest_post.title }}</h2>
      <p class="post-meta">Published on {{ latest_post.date | date: "%B %d, %Y" }}</p>
      <div class="excerpt">
        {{ latest_post.excerpt | strip_html | truncatewords: 50 }}
      </div>
      <a class="read-more" href="{{ latest_post.url }}">Read More</a>
    </article>
  {% else %}
    <p>No posts available yet. Check back soon!</p>
  {% endif %}
</div>