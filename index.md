---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: page
title: Home
---

# Projects

<style>
.projects {
  display: grid;
  gap: 2rem;
  grid-template-columns: 1fr; /* mobile default */
}

@media (min-width: 600px) {
  .projects {
    grid-template-columns: repeat(2, 1fr);
  }
}
</style>

<div class="projects">
  {% assign sorted_projects = site.projects | sort: "year" | reverse %}
  {% for project in sorted_projects limit:4 %}
    <div class="project-card">
      <h4>{{ project.title }}</h4>

      <p>
        <a href="{{ project.link | default: project.url | relative_url }}">
          → View project
        </a>
      </p>

      <p>{{ project.year }} – {{ project.description }}</p>

    </div>
  {% endfor %}
</div>
