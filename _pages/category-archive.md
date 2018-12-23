---
layout: archive
permalink: /categories/
title: "Posts by Category"
author_profile: true
---

[Posts - by Year Collection](https://hannahpu.github.io/collection-archive/)

[Posts - by Tags](https://hannahpu.github.io/tags/)


{% include group-by-array collection=site.posts field="categories" %}

{% for category in group_names %}
  {% assign posts = group_items[forloop.index0] %}
  <h2 id="{{ category | slugify }}" class="archive__subtitle">{{ category }}</h2>
  {% for post in posts %}
    {% include archive-single.html %}
  {% endfor %}
{% endfor %}
