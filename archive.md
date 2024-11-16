---
layout: page
title: Archive
permalink: /archive/
---
<h1>Archive</h1>
<div class="archive">
  {% assign posts_by_year = site.posts | group_by_exp: "post", "post.date | date: '%Y'" %}
  {% for year in posts_by_year %}
    <h2>{{ year.name }}</h2>
    {% assign posts_by_month = year.items | group_by_exp: "post", "post.date | date: '%B'" %}
    {% for month in posts_by_month %}
      <h3>{{ month.name }}</h3>
      <ul>
        {% for post in month.items %}
          <li><a href="{{ post.url }}">{{ post.title }}</a></li>
        {% endfor %}
      </ul>
    {% endfor %}
  {% endfor %}
</div>