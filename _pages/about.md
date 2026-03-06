---
layout: about
title: About
permalink: /
subtitle: alinepaes (at) ic.uff.br 


profile:
  align: right
  image: prof_pic.jpg
  image_circular: false # crops the image to make it circular
  more_info: 
     


selected_papers: false # includes a list of papers marked as "selected={true}"
social: true # includes social icons at the bottom of the page
---

I am an Associate Professor of Artificial Intelligence at the <a href="https://www.ic.uff.br/"> Institute of Computing </a> of the <a href="https://www.uff.br/"> Universidade Federal Fluminense (UFF) </a>, located in the charming city of <a href="https://g.co/kgs/4Gt8DdR"> Niterói </a>, RJ, Brazil. I am a core faculty member of the Graduate Program in Computer Science at IC/UFF—rated CAPES 7, the highest level of excellence in the country— where I lead the Machine Learning and Language Learning <a href="https://melll-uff.github.io/">(MeLLL-UFF) </a>research group. I serve as an Associate Editor for several prestigious journals, including Springer Machine Learning, Cambridge NLP, SBC JBCS, and IBERAMIA Inteligência Artificial.

My work is supported by a CNPq Research Productivity Grant and a FAPERJ Young Scientist Grant. I am also a member of three CNPq National Institutes of Science and Technology (INCTs): the National Institute of AI (IAIA), TILD-IAR (Responsible AI for Computational Linguistics), and IAPROBEM (AI for Social Good). Additionally, I am a member of the <a href ="https://brasileiraspln.com/"> Brasileiras em PLN (Brazilian Women in NLP)</a> group.

My recent research focuses on Machine Learning for Natural Language Processing (NLP), Relational ML, and AI for Social Impact. My current research interests include:
 - Multilingual Language Models and Generative AI 
 - Knowledge-enhanced and Low-resource ML for NLP
 - Figurative Language
 - Text simplification
 - Generative AI for Financial Assets Analyses
 - Reasoning with NLP and Relational ML 
 - Transfer Learning for Statistical Relational Models
 - Detecting fake news, hate speech, gender bias, and online manipulation.

I am always open to new collaborations—please feel free to contact me if you are interested in these topics.

{% if site.announcements.enabled %}

<hr>

<h2>News</h2>

<div class="row row-cols-1 row-cols-md-1 g-4">
  {% assign news = site.news | sort: "date" | reverse %}
  {% for item in news limit: site.announcements.limit %}
    <div class="col">
      <div class="card hoverable">
        <div class="card-body">
          <h5 class="card-title">{{ item.title }}</h5>
          <h6 class="card-subtitle mb-2 text-muted">
            {{ item.date | date: "%B %d, %Y" }}
          </h6>
          <p class="card-text">
            {{ item.content | strip_html | truncatewords: 30 }}
          </p>
          <a href="{{ item.url }}" class="card-link">Read more →</a>
        </div>
      </div>
    </div>
  {% endfor %}
</div>

<div style="margin-top: 1rem;">
  <a href="/news/" class="btn btn-outline-primary btn-sm">
    View all announcements
  </a>
</div>

{% endif %}



