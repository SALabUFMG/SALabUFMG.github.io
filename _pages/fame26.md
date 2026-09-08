---
layout: page
title: FAME '26 (5ª Edição)
permalink: /FAME26/
description:
nav: false
nav_order: 
horizontal: false
social: true  # includes social icons at the bottom of the page
---

<!-- pages/fame26.md -->

### Patrocínio
Patrocinado por:

<div style="display: flex; justify-content: space-between; align-items: center;">
    <div style="width: 45%;">
        <a href="https://geminisports.ai">
            <img id='gemini-logo' style="width: 100%;" src="../assets/img/FoF/logo_gemini_original.png" alt="Gemini Sports Analytics logo">
        </a>
    </div>
</div> <br/>

Faça parte do nosso evento extraordinário e mostre o compromisso da sua marca com a excelência.
<a href='../sponsorship/'>Clique aqui</a> para explorar nossos pacotes exclusivos de patrocínio e descubra como podemos
criar uma parceria personalizada que esteja alinhada com seus objetivos.

Entre em contato por meio do email <a href="mailto:salab.dcc.ufmg@gmail.com">salab.dcc.ufmg@gmail.com</a> para mais detalhes sobre ser avançar nesta parceria.

<hr>


### Ingressos
Mais informações sobre os ingressos serão divulgadas em breve. Fique atento às nossas redes sociais para não perder nenhuma atualização!

Abertura das vendas: <b>8 de setembro de 2026<b>

<hr>

### Sobre o evento
- **Data:** 28 de Setembro de 2026
- **Local:** <a href='https://maps.app.goo.gl/DvN4WFp6hKDvHia36'>Centro de Atividades Didáticas 3, UFMG Campus Pampulha</a> - Belo Horizonte / MG
- **Horário:** 8:30 às 18:00

O Sports Analytics Lab (SALab), do Departamento de Ciência da Computação da UFMG, convida você para a quinta edição do "FAME: Football Analytics and Modeling Experience". 
Mais do que um evento, o FAME é o ponto de encontro entre a ciência de dados e a paixão pelo futebol. 
Nosso propósito é integrar alunos, acadêmicos e especialistas do mercado em um ambiente de troca mútua, focado nas tendências e na realidade do Football Analytics. Prepare-se para uma imersão com palestras, painéis e apresentações de trabalhos.

Fique atento nas nossas redes sociais, pois a programação oficial ainda será revelada!

<hr>


<div class="projects">
{%- if site.enable_project_categories and page.display_categories %}
  <!-- Display categorized projects -->
  {%- for category in page.display_categories %}
  <h2 class="category">{{ category }}</h2>
  {%- assign categorized_projects = site.fame26 | where: "category", category -%}
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
{%- assign sorted_projects = site.fame26 | sort: "importance" -%}
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