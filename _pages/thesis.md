---
layout: category
taxonomy: research
permalink: /thesis/
title: "Thesis progess Posts."
author_profile: true
header: 
    image: "/images/there_will.jpeg"
---

{% include group-by-array collection=site.posts field="tags" %}

{% for tags in group_names %}

{% if page.category == "research" %}

  {% assign posts = group_items[forloop.index0] %}
  <h2 id="{{ tag | slugify }}" class="archive__subtitle">{{ tag }}</h2>

  {% for post in posts %}
    {% include archive-single.html %}
  {% endfor %}

{% endif %}

{% endfor %}