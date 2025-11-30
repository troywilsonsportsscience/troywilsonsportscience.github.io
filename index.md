---
layout: splash
title: "Applied sport science, strength & conditioning, and data analytics."
permalink: /
header:
  overlay_color: "#0b1120"
  overlay_filter: "0.6"
  overlay_image: "/assets/img/hero-profile.jpg"
  actions:
    - label: "View Services"
      url: "/services/"
    - label: "View Projects"
      url: "/projects/"
intro:
  - excerpt: "Bridging applied sport science, strength and conditioning, and data analytics to help athletes, coaches, and organizations make better decisions."
feature_row:
  - title: "Performance Services"
    excerpt: "Testing, monitoring, and strength & conditioning support for individuals and teams."
    url: "/services/"
    btn_label: "View services"
    btn_class: "btn--primary"
  - title: "Sport Science Projects"
    excerpt: "Dashboards, KPIs, and analytical tools built from real high-performance environments."
    url: "/projects/"
    btn_label: "See projects"
    btn_class: "btn--primary"
  - title: "Data-Driven Content"
    excerpt: "Articles and resources on testing, monitoring, and training decisions."
    url: "/blog/"
    btn_label: "Read the blog"
    btn_class: "btn--primary"
---

{% include feature_row id="intro" type="center" %}

{% include feature_row %}

## Featured projects

<ul class="project-list">
  {% assign featured_projects = site.projects | where_exp: "item", "item.featured == true" | slice: 0, 3 %}
  {% for project in featured_projects %}
  <li>
    <a href="{{ project.url | relative_url }}"><strong>{{ project.title }}</strong></a><br>
    <span>{{ project.summary }}</span>
  </li>
  {% endfor %}
</ul>

## Latest articles

<ul class="post-list">
  {% for post in site.posts limit:3 %}
  <li>
    <a href="{{ post.url | relative_url }}"><strong>{{ post.title }}</strong></a>
    <span> — {{ post.date | date: "%b %-d, %Y" }}</span><br>
    <span>{{ post.excerpt | strip_html | truncate: 140 }}</span>
  </li>
  {% endfor %}
</ul>

## Ready to talk?

- Discuss services and packages: [Services](/services/)
- Book a call: [Booking link](https://calendly.com/your-link-here)
- Or use the [contact form](/contact/)
