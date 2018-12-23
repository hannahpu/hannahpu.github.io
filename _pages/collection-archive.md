---
layout: archive
title: "Posts by Year"
permalink: /collection-archive/
author_profile: true
---

[Posts - by Categories](https://hannahpu.github.io/categories/)

[Posts - by Tags](https://hannahpu.github.io/tags/)

{% assign postsByYear = site.posts | group_by_exp:"post", "post.date | date: '%Y'"  %}
{% for year in postsByYear %}
  <h2 id="{{ year.name | slugify }}" class="archive__subtitle">{{ year.name }}</h2>
  {% for post in year.items %}
    {% include archive-single.html %}
  {% endfor %}
{% endfor %}