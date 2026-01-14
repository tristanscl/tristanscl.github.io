---
layout: page
title: Projects
permalink: /projects/
---

{% assign sorted_projects = site.projects | sort: "year" | reverse %}
{% for project in sorted_projects %}
  <h2>{{ project.title }}</h2>

  <p class="project-year"></p>

  <p>{{ project.year }} - {{ project.description }}</p>

  <p>
    <a href="{{ project.link | default: project.url | relative_url }}">
      → View project
    </a>
  </p>
{% endfor %}
