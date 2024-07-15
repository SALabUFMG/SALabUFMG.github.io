---
layout: page
title: FAME '24 (3ª Edição)
permalink: /FAME24/
description:
nav: false
nav_order: 
horizontal: false
social: true  # includes social icons at the bottom of the page
---

<!-- pages/fame24.md -->

### Ingressos
A ser anunciado.

<hr>

### Sobre o evento
- **Data:** 05/09/2024
- **Local:** <a href='https://maps.app.goo.gl/DvN4WFp6hKDvHia36'>Centro de Atividades Didáticas 3</a>, UFMG - Campus Pampulha
- **Horário:** 8:30 às 18:30

<hr>

O <b>Sports Analytics Lab (SALab)</b> do Departamento de Ciência da Computação da UFMG tem o prazer de apresentar a terceira edição do 
<b>"FAME: Football Analytics and Modeling Experience"</b>, um evento dinâmico destinado a unir a <b>ciência de dados e o futebol</b>. 
O objetivo principal deste evento é criar um ambiente enriquecedor onde alunos, professores e profissionais da indústria do futebol 
possam se conectar, trocar experiências, construir conhecimento e se informar sobre a realidade atual da área de Football Analytics. 
A programação completa do FAME contará com <b>palestras, painéis e apresentação de trabalhos submetidos</b>. A programação do evento ainda será anunciada!
<hr>
<div class="projects">
{%- if site.enable_project_categories and page.display_categories %}
  <!-- Display categorized projects -->
  {%- for category in page.display_categories %}
  <h2 class="category">{{ category }}</h2>
  {%- assign categorized_projects = site.fame24 | where: "category", category -%}
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
  {%- assign sorted_projects = site.fame24 | sort: "importance" -%}
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