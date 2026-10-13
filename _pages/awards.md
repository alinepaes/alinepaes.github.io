---
layout: page
permalink: /awards/
title: Awards & Distinctions
description: Research fellowships, paper awards, and recognitions received by my students and me over the last ten years (2017–2026).
nav: true
nav_order: 7
---

{% comment %} Data lives in _data/awards.yml — edit entries there. Styles: _sass/_awards.scss {% endcomment %}
{% assign a = site.data.awards %}

<div class="awards">

  <!-- Fellowships & distinctions -->
  <h2 class="awards-heading">Research fellowships &amp; distinctions</h2>
  <div class="fellow-grid">
    {% for f in a.fellowships %}
      <article class="fellow-card">
        <div class="fellow-icon"><i class="{{ f.icon }}" aria-hidden="true"></i></div>
        <div class="fellow-body">
          <div class="fellow-top">
            <span class="fellow-agency">{{ f.agency }}</span>
            <span class="fellow-period">{{ f.period }}</span>
          </div>
          <h3 class="fellow-title">{{ f.title }}</h3>
          {% if f.note %}<p class="fellow-note">{{ f.note }}</p>{% endif %}
          {% if f.project %}<p class="fellow-project"><span>Project</span> {{ f.project }}</p>{% endif %}
        </div>
      </article>
    {% endfor %}
  </div>

  <!-- Paper awards -->
  <h2 class="awards-heading">Paper awards</h2>
  <div class="aw-timeline">
    {% for y in a.paper_awards %}
      <div class="aw-row">
        <div class="aw-row-year">{{ y.year }}</div>
        <ul class="aw-row-body">
          {% for i in y.items %}
            <li class="aw-item">
              <span class="medal medal-{{ i.rank }}" aria-hidden="true"><i class="fa-solid {% if i.rank == 'mention' %}fa-award{% else %}fa-medal{% endif %}"></i></span>
              <div>
                <div class="aw-title">{{ i.award }} <span class="aw-venue">· {{ i.venue }}</span></div>
                {% if i.paper %}<div class="aw-paper">{{ i.paper }}</div>{% endif %}
              </div>
            </li>
          {% endfor %}
        </ul>
      </div>
    {% endfor %}
  </div>
  <p class="aw-legend">
    <span class="medal medal-gold"><i class="fa-solid fa-medal"></i></span> best / 1st place
    <span class="medal medal-silver"><i class="fa-solid fa-medal"></i></span> 2nd place
    <span class="medal medal-bronze"><i class="fa-solid fa-medal"></i></span> 3rd place
    <span class="medal medal-mention"><i class="fa-solid fa-award"></i></span> honorable mention
  </p>

  <!-- Student awards -->
  <h2 class="awards-heading">Awards to students I supervised</h2>
  <div class="student-grid">
    {% for s in a.student_awards %}
      <article class="student-card">
        <div class="student-top">
          <span class="medal medal-{{ s.rank }}" aria-hidden="true"><i class="fa-solid {% if s.rank == 'mention' %}fa-award{% else %}fa-medal{% endif %}"></i></span>
          <span class="student-year">{{ s.year }}</span>
        </div>
        <h3 class="student-name">{{ s.student }}</h3>
        <p class="student-award">{{ s.award }}</p>
        <p class="student-meta">{{ s.level }} · {{ s.role }}</p>
      </article>
    {% endfor %}
  </div>

  <!-- Teaching honors -->
  <h2 class="awards-heading">Teaching honors</h2>
  <ul class="honor-list">
    {% for t in a.teaching_honors %}
      <li><span class="honor-year">{{ t.year }}</span><i class="fa-solid fa-graduation-cap" aria-hidden="true"></i><span>{{ t.award }} <span class="aw-venue">· {{ t.org }}</span></span></li>
    {% endfor %}
  </ul>

  {% if a.earlier %}
  <details class="aw-earlier">
    <summary>Earlier awards (before 2017)</summary>
    <ul class="honor-list">
      {% for e in a.earlier %}
        <li><span class="honor-year">{{ e.year }}</span><i class="fa-solid fa-trophy" aria-hidden="true"></i><span>{{ e.award }}</span></li>
      {% endfor %}
    </ul>
  </details>
  {% endif %}

</div>
