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

I am an Associate Professor of Artificial Intelligence at the <a href="https://www.ic.uff.br/"> Institute of Computing </a> of the <a href="https://www.uff.br/"> Universidade Federal Fluminense (UFF) </a>, located in the charming city of <a href="https://g.co/kgs/4Gt8DdR"> Niterói </a>, RJ, Brazil. I am affiliated with the Graduate Program in Computer Science at IC/UFF (Maximu  Excellence Level from CAPES), where I lead the Machine Learning and Language Learning <a href="https://github.com/MeLLL-UFF">(MeLLL-UFF) </a>research group.  I hold a productivity research grant (level E) from CNPq and a young scientist research grant from FAPERJ. I am a member of the following CNPq National Institutes of Science and Technology (INCT): National Institute of AI (IAIA), National Institute of Science and Technology in Responsible Artificial Intelligence for Computational Linguistics, Information Processing, and Information Dissemination (TILD-IAR), and National Institute of AI for Social Good (IAPROBEM). I am also a member of the <a href ="https://brasileiraspln.com/"> Brazilian Women in NLP group (Brasileiras em PLN)</a>. Check out our first free and online <a href="https://brasileiraspln.com/livro-pln/"> book </a> about NLP in Portuguese. 

My recent research has primarily focused on machine learning for natural language processing, relational machine learning, and AI for positive social impact. Currently, I am interested in:
 - Multilingual Language Models and Generative AI 
 - Knowledge-enhanced ML for NLP
 - Low-resource ML for NLP
 - Figurative Language
 - Text simplification
 - Generative AI for Financial Assets Analyses
 - Reasoning with NLP and Relational ML 
 - Transfer Learning for Statistical Relational Models
 - Automatic detection of lousy behavior like fake news, hate speech, gender bias, and persuasion for negative manipulation.

If you want to collaborate on those themes, feel free to contact me

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



