---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: page
title: Projects
---

Here are some sample projects I wanted to showcase. I might add more in the future when I have time to write a page for them. I tried to pick them to get the most variety of topics covered.

<div>
  {% assign sorted_projects = site.projects | sort: "year" | reverse %}
  {% for project in sorted_projects %}
    <div class="project-card">
      <h3>{{ project.title }}</h3>

      <p>
        <a href="{{ project.link | default: project.url | relative_url }}">
          → View project
        </a>
      </p>

      <p>{{ project.year }} – {{ project.description }}</p>

    </div>
  {% endfor %}
</div>