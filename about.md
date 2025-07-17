---
layout: default
title: People
permalink: /about.html
---

# Who are we?

At the moment we are a group of people at UCL interested to promote Linux across the university.

<div class="row-fluid">
{% for member in site.data.members %}
{% include member.html member=member%}
  {% cycle '', '', '', '</div>' %}
  {% cycle '', '', '', '<div class="row-fluid">' %}
{% endfor %}
</div>

