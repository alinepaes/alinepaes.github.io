---
layout: page
permalink: /teaching/
title: Teaching
description: Undergraduate and graduate courses I have taught at UFF. Course materials are shared privately with enrolled students via Google Classroom.
nav: true
nav_order: 5
---

{% comment %} Data lives in _data/teaching.yml — edit courses there. Styles: _sass/_teaching.scss {% endcomment %}
{% assign t = site.data.teaching %}
{% assign grad = t.courses | where: "level", "grad" %}
{% assign undergrad = t.courses | where: "level", "undergrad" %}

<div class="teaching">

  {% assign groups = "grad,undergrad" | split: "," %}
  {% for lvl in groups %}
    {% if lvl == "grad" %}
      {% assign list = grad %}{% assign heading = "Graduate" %}
    {% else %}
      {% assign list = undergrad %}{% assign heading = "Undergraduate" %}
    {% endif %}

    <h2 class="teaching-heading">{{ heading }}</h2>
    <div class="course-grid">
      {% for c in list %}
        <article class="course-card course-{{ c.level }}" aria-label="{% if c.level == 'grad' %}Graduate{% else %}Undergraduate{% endif %} course">
          <div class="course-top">
            <span class="course-level">{{ c.program }}</span>
            <span class="course-count" title="Times offered since 2020">{{ c.semesters.size }}×</span>
          </div>
          <h3 class="course-name">{{ c.name }}</h3>
          <p class="course-desc">{{ c.description }}</p>
          <ul class="course-semesters" aria-label="Semesters offered">
            {% for s in c.semesters %}
              {% if t.remote_semesters contains s %}
                <li class="remote" title="Online (COVID-19)">{{ s }}</li>
              {% else %}
                <li>{{ s }}</li>
              {% endif %}
            {% endfor %}
          </ul>
        </article>
      {% endfor %}
    </div>
  {% endfor %}

  <h2 class="teaching-heading">Before 2020</h2>
  <div class="course-earlier">
    {% for name in t.earlier %}<span>{{ name }}</span>{% endfor %}
  </div>

  <p class="teaching-note"><span class="legend-remote"></span> Dashed semesters were taught online during the COVID-19 pandemic.</p>
</div>
