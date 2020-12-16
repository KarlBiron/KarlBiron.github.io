---
layout: archive
permalink: /blogs_page/
title: "Blogs on Cyber Security Career, Certification, Publications, and Thoughts"
author_profile: structured
header:
  images: "/images/fort point.png"
---

{% include base_path %}
{% include group-by-array collection=site.posts field="tags" %}

{% for tag in group_names %}
  {% assign posts = group_items[forloop.index0] %}
  <h2 id="{{ tag | slugify }}" class="archive__subtitle">{{ tag }}</h2>
  {% for post in posts %}
    {% include archive-single.html %}
  {% endfor %}
{% endfor %}
