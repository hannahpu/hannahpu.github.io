---
layout: archive
permalink: /tags/
title: "Posts by Tag"
author_profile: true
---

[Posts - by Year Collection](https://hannahpu.github.io/collection-archive/)

[Posts - by Categories](https://hannahpu.github.io/categories/)

{% include group-by-array collection=site.posts field="tags" %}

{% for tag in group_names %}
  {% assign posts = group_items[forloop.index0] %}
  <h2 id="{{ tag | slugify }}" class="archive__subtitle">{{ tag }}</h2>
  {% for post in posts %}
    {% include archive-single.html %}
  {% endfor %}
{% endfor %}
