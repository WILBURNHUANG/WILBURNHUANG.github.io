---
layout: category
taxonomy: review
permalink: /movie_review/
title: "Movie review Posts."
author_profile: true
header: 
    image: "/images/there_will.jpeg"
---

{% include group-by-array collection=site.posts field="tags" %}

{% for tags in group_names %}

{% if page.category == "review" %}

  {% assign posts = group_items[forloop.index0] %}
  <h2 id="{{ tag | slugify }}" class="archive__subtitle">{{ tag }}</h2>

  {% for post in posts %}
    {% include archive-single.html %}
  {% endfor %}

{% endif %}

{% endfor %}