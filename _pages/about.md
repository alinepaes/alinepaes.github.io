---
layout: about
title: About
permalink: /
subtitle: Associate Professor of Artificial Intelligence · Institute of Computing, UFF

profile:
  align: right
  image: prof_pic_portrait.jpg
  image_circular: false # crops the image to make it circular
  more_info:

selected_papers: false # includes a list of papers marked as "selected={true}"
social: true # includes social icons (incl. email) at the bottom of the page
---

I am an Associate Professor of Artificial Intelligence at the <a href="https://www.ic.uff.br/">Institute of Computing</a> of the <a href="https://www.uff.br/">Universidade Federal Fluminense (UFF)</a>, in the charming city of <a href="https://g.co/kgs/4Gt8DdR">Niterói</a>, RJ, Brazil. I am a core faculty member of the <a href="https://www.pgc.uff.br/pos-graduacao">Graduate Program in Computer Science</a> at IC/UFF — rated CAPES 7, the highest level of excellence in the country — where I lead the Machine Learning and Language Learning (<a href="https://melll-uff.github.io/">MeLLL-UFF</a>) research group.

My research focuses on Machine Learning for Natural Language Processing (NLP), Relational ML, and AI for Social Impact. My current interests include:

- Multilingual language models and generative AI
- Knowledge-driven transfer and adaptation for low-resource NLP
- Figurative language
- Text simplification
- Generative AI for financial asset analysis
- Reasoning with NLP and relational ML
- Transfer learning for statistical relational models
- Detection of fake news, hate speech, gender bias, propaganda and online manipulation

**Service.** I am an Associate Editor of Springer Machine Learning, Cambridge NLP, SBC JBCS and IBERAMIA Inteligência Artificial, and a member of the <a href="https://www.iberamia.org/iberamia/junta-ejecutiva/">IBERAMIA Steering Committee</a>. I have served as Program Chair of CTDIAC 2014, ENIAC 2017, KDMiLe 2022/2023, BRACIS 2024 and STIL 2026, and as Tutorial Co-chair of EACL 2026. In 2028, I will serve as General Chair of PROPOR. I was previously a member of the SBC Special Committees on AI (CEIA) and NLP (CE-PLN).

**Funding and networks.** My work is supported by a CNPq Research Productivity Grant and a FAPERJ Young Scientist Grant. I am a member of three National Institutes of Science and Technology (INCTs) funded by CNPq — the <a href="https://inct-iaia.vercel.app/institutions">National Institute of AI (IAIA)</a>, <a href="https://tildiar.dcc.ufmg.br/">TILD-IAR</a> (Responsible AI for Computational Linguistics, Treatment and Dissemination of Information) and IAPROBEM (AI for Social Good) — and of the <a href="https://brasileiraspln.com/">Brasileiras em PLN</a> (Brazilian Women in NLP) group.

I am always open to new collaborations — please feel free to contact me if you are interested in these topics.

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



