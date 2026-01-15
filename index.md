---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: page
title: Projects
---

<div>
  {% assign sorted_projects = site.projects | sort: "year" | reverse %}
  {% for project in sorted_projects %}
    <div class="project-card">
      <h2>{{ project.title }}</h2>

      <p>
        <a href="{{ project.link | default: project.url | relative_url }}">
          → View project
        </a>
      </p>

      <p>{{ project.year }} – {{ project.description }}</p>

    </div>
  {% endfor %}
</div>
