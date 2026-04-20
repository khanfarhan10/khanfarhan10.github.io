---
layout: archive
permalink: /WoC/
title: "Community Archive"
author_profile: true
header:
  image: "/assets/images/ai1.png"
---

This page preserves earlier community writing and mentoring content from a past open-source community program.

It is kept online as archive material and does not represent my current professional profile.

<div class="grid__wrapper">
  {% assign collection = 'woc' %}
  {% assign posts = site[collection] | reverse %}
  {% for post in posts %}
    {% include archive-single.html type="grid" %}
  {% endfor %}
</div>
