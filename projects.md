---
title: "Projects"
permalink: /projects/
---

## Sport science and data projects

These projects show how I approach testing, monitoring, and decision-support in real environments.

<ul class="project-list">
  {% assign sorted_projects = site.projects | sort: "title" %}
  {% for project in sorted_projects %}
  <li>
    <a href="{{ project.url | relative_url }}"><strong>{{ project.title }}</strong></a><br>
    <span>{{ project.summary }}</span>
  </li>
  {% endfor %}
</ul>
