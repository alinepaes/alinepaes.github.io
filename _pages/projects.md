---
layout: page
title: Projects
permalink: /projects/
description: Funded research projects I lead or take part in.
nav: true
nav_order: 3
display_categories: [Current, Past]
---

<!-- pages/projects.md — list layout, see _includes/project_row.liquid and _sass/_projects.scss -->
<div class="projects projects-list">
{% if site.enable_project_categories and page.display_categories %}
  {% for category in page.display_categories %}
    {% assign categorized_projects = site.projects | where: "category", category %}
    {% if categorized_projects.size > 0 %}
      {% assign sorted_projects = categorized_projects | sort: "importance" %}
      <h2 class="category" id="{{ category | slugify }}">{{ category }} <span class="category-count">{{ sorted_projects.size }}</span></h2>
      {% for project in sorted_projects %}
        {% include project_row.liquid %}
      {% endfor %}
    {% endif %}
  {% endfor %}
{% else %}
  {% assign sorted_projects = site.projects | sort: "importance" %}
  {% for project in sorted_projects %}
    {% include project_row.liquid %}
  {% endfor %}
{% endif %}
</div>
