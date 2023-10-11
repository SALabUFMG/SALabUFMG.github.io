---
layout: page
title: FAME '23 (2ª Edição)
permalink: /FAME23/
description:
nav: false
nav_order: 
horizontal: false
---

<!-- pages/fame23.md -->
<div style="display: flex; justify-content: space-between; align-items: center;">
    <div style="font-size: 24px;">
        Patrocinado pela <a href='https://geminisports.co/'>Gemini Sports Analytics</a>
    </div>
    <div style="width: 40%;">
        {% include figure.html path="assets/img/FAME/2023/gemini-header.png" class="img-fluid rounded z-depth-1"%}
    </div>
</div>
<hr>
### Sobre o evento
- **Data:** 17/11/2023
- **Local:** <a href='https://maps.app.goo.gl/DvN4WFp6hKDvHia36'>Centro de Atividades Didáticas 3</a> – Auditório B101/102, UFMG - Campus Pampulha
- **Horário:** 9:00 às 17:00
- **Ingressos:** <a href='https://www.sympla.com.br/fame-23-football-analytics-modelling-and-experience__2197311'>Link</a> pelo Sympla! O ingresso terá 
novamente o valor simbólico de R$5,00, de modo a evitarmos que pessoas 
registrem-se para o evento e não compareçam. Como no ano passado, todo o valor arrecadado será doado para a Casa de Amparo Amigos da Vida (CAMAV).
<hr>

O <b>Sports Analytics Lab (SALab)</b> do Departamento de Ciência da Computação da UFMG tem o prazer de apresentar a segunda edição do 
<b>"FAME: Football Analytics and Modeling Experience"</b>, um evento dinâmico destinado a unir a <b>ciência de dados e o futebol</b>. 
O objetivo principal deste evento é criar um ambiente enriquecedor onde alunos, professores e profissionais da indústria do futebol 
possam se conectar, trocar experiências, construir conhecimento e se informar sobre a realidade atual da área de Football Analytics. 
A programação completa do FAME contará com <b>palestras, painéis e apresentação de trabalhos submetidos</b>. Em breve, divulgaremos 
a programação do evento!
<hr>

<div class="projects">
{%- if site.enable_project_categories and page.display_categories %}
  <!-- Display categorized projects -->
  {%- for category in page.display_categories %}
  <h2 class="category">{{ category }}</h2>
  {%- assign categorized_projects = site.fame23 | where: "category", category -%}
  {%- assign sorted_projects = categorized_projects | sort: "importance" %}
  <!-- Generate cards for each project -->
  {% if page.horizontal -%}
  <div class="container">
    <div class="row row-cols-2">
    {%- for project in sorted_projects -%}
      {% include projects_horizontal.html %}
    {%- endfor %}
    </div>
  </div>
  {%- else -%}
  <div class="grid">
    {%- for project in sorted_projects -%}
      {% include projects.html %}
    {%- endfor %}
  </div>
  {%- endif -%}
  {% endfor %}

{%- else -%}
<!-- Display projects without categories -->
  {%- assign sorted_projects = site.fame23 | sort: "importance" -%}
  <!-- Generate cards for each project -->
  {% if page.horizontal -%}
  <div class="container">
    <div class="row row-cols-2">
    {%- for project in sorted_projects -%}
      {% include projects_horizontal.html %}
    {%- endfor %}
    </div>
  </div>
  {%- else -%}
  <div class="grid">
    {%- for project in sorted_projects -%}
      {% include projects.html %}
    {%- endfor %}
  </div>
  {%- endif -%}
{%- endif -%}
</div>