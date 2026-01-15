---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: page
title: Projects
---


<div class="projects">
  {% assign sorted_projects = site.projects | sort: "year" | reverse %}
  {% for project in sorted_projects %}
  <!-- put limit:3 or the number of projects you want to be displayed after sorted_projects if needed -->
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
