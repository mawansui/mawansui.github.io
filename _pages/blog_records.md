---
layout: archive
title: "Blog posts"
permalink: /blog/
author_profile: true
---

Here you may find a collection of my posts related to chemoinformatics and things I do at work. Enjoy!

{% include base_path %}

{% for post in site.blogposts reversed %}
  {% include archive-single.html %}
{% endfor %}