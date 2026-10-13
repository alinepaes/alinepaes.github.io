---
layout: page
permalink: /service/
title: Service
description: Advisory committees, editorial work, event organization, peer review and examination committees over the last ten years (2017–2026).
nav: true
nav_order: 6
---

{% comment %} Data lives in _data/service.yml — edit entries there. Styles: _sass/_service.scss {% endcomment %}
{% assign s = site.data.service %}

<div class="service">

  <nav class="service-toc" aria-label="Sections">
    <a href="#advisory">Advisory &amp; grant review</a>
    <a href="#editorial">Editorial boards</a>
    <a href="#organization">Event organization</a>
    <a href="#program-committees">Program committees</a>
    <a href="#journals">Journal reviewing</a>
    <a href="#examination">Examination committees</a>
  </nav>

  <!-- Advisory committees & grant review -->
  <h2 class="service-heading" id="advisory">Advisory committees &amp; grant review</h2>
  <div class="service-cols">
    <div class="svc-card">
      <h3 class="svc-card-title">Committees</h3>
      <ul class="svc-list">
        {% for a in s.advisory %}
          <li><span class="svc-year">{{ a.year }}</span><span><strong>{{ a.role }}</strong><br><span class="svc-muted">{{ a.org }}</span></span></li>
        {% endfor %}
      </ul>
    </div>
    <div class="svc-card">
      <h3 class="svc-card-title">Grant proposal reviewer</h3>
      <ul class="svc-list">
        {% for g in s.grant_review %}
          <li><span class="svc-year">{{ g.period }}</span><span>{{ g.org }}</span></li>
        {% endfor %}
      </ul>
    </div>
  </div>

  <!-- Editorial boards -->
  <h2 class="service-heading" id="editorial">Editorial boards</h2>
  <div class="svc-grid">
    {% for e in s.editorial %}
      <article class="svc-card svc-accent">
        <span class="svc-kicker">Editorial board · since {{ e.since }}</span>
        <h3 class="svc-name">{{ e.journal }}</h3>
      </article>
    {% endfor %}
  </div>

  <!-- Event organization -->
  <h2 class="service-heading" id="organization">Event organization</h2>
  <div class="svc-timeline">
    {% for y in s.organization %}
      <div class="svc-row">
        <div class="svc-row-year">{{ y.year }}</div>
        <ul class="svc-row-body svc-org">
          {% for i in y.items %}
            <li><span class="svc-role">{{ i.role }}</span> {{ i.event }}</li>
          {% endfor %}
        </ul>
      </div>
    {% endfor %}
  </div>

  <!-- Program committees & conference reviewing -->
  <h2 class="service-heading" id="program-committees">Program committees &amp; conference reviewing</h2>
  <div class="svc-timeline">
    {% for y in s.program_committees %}
      <div class="svc-row">
        <div class="svc-row-year">{{ y.year }}</div>
        <ul class="svc-row-body svc-chips">
          {% for v in y.venues %}
            <li class="{{ v.role }}" title="{% if v.role == 'pc' %}Program committee member{% else %}Reviewer{% endif %}">{{ v.name }}</li>
          {% endfor %}
        </ul>
      </div>
    {% endfor %}
  </div>
  <p class="svc-legend">
    <span class="svc-chip-sample"></span> program committee member
    <span class="svc-chip-sample reviewer"></span> reviewer / sub-reviewer
  </p>

  <!-- Journal reviewing -->
  <h2 class="service-heading" id="journals">Journal reviewing</h2>
  <p class="svc-note">Grouped by the year I first reviewed for each journal; journals I started reviewing for before 2017 and still review for are listed last.</p>
  <div class="svc-timeline">
    {% for y in s.journals %}
      <div class="svc-row">
        <div class="svc-row-year">{% if y.year == "Earlier" %}Before<br>2017{% else %}{{ y.year }}{% endif %}</div>
        <ul class="svc-row-body svc-chips svc-chips-plain">
          {% for j in y.journals %}
            <li>{{ j }}</li>
          {% endfor %}
        </ul>
      </div>
    {% endfor %}
  </div>

  <!-- Examination committees -->
  <h2 class="service-heading" id="examination">Examination committees</h2>
  <div class="svc-grid svc-grid-3">
    {% for c in s.examination %}
      <article class="svc-card svc-exam">
        <div class="svc-exam-top">
          <span class="svc-exam-num">{{ c.count }}</span>
          <span class="svc-exam-since">2017–2026</span>
        </div>
        <h3 class="svc-exam-type">{{ c.type }}</h3>
        <ul class="svc-inst">
          {% for i in c.institutions %}
            <li>{{ i.name }}{% if i.count > 1 %}<span>{{ i.count }}</span>{% endif %}</li>
          {% endfor %}
        </ul>
      </article>
    {% endfor %}
  </div>

</div>
