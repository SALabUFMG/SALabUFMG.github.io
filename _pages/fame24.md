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

### Patrocínio
Patrocinado por: 
<div style="display: flex; justify-content: space-between; align-items: center;">
    <div style="width: 45%;">
        <a href="https://geminisports.ai">
            <img id='gemini-logo' style="width: 100%;" src="../assets/img/FoF/logo_gemini_original.png" alt="Gemini Sports Analytics logo">
        </a>
    </div>
    <div style="width: 45%;">
        <a href="https://geminisports.ai">
            <img id='onefan-logo' style="width: 100%;" src="../assets/img/FoF/logo_onefan_original.png" alt="OneFan logo">
        </a>
    </div>
</div>

Faça parte do nosso evento extraordinário e mostre o compromisso da sua marca com a excelência. 
<a href='../sponsorship/'>Clique aqui</a> para explorar nossos pacotes exclusivos de patrocínio e descubra como podemos 
criar uma parceria personalizada que esteja alinhada com seus objetivos.


### Ingressos
Garanta seu ingresso já para esse evento incrível! <a href='https://www.sympla.com.br/evento/future-of-football-conference-fame-24-business-of-global-football-ufmg-nyu/2559817'>Clique aqui</a> para comprar seu ingresso e garantir seu lugar.

<hr>

### Sobre o evento
- **Data:** 05 de Setembro de 2024
- **Local:** <a href='https://maps.app.goo.gl/DvN4WFp6hKDvHia36'>Centro de Atividades Didáticas 3</a>, UFMG - Campus Pampulha
- **Horário:** 8:30 às 18:30

<hr>

O <b>Sports Analytics Lab (SALab)</b> do Departamento de Ciência da Computação da UFMG tem o prazer de apresentar a terceira edição do 
<b>"FAME: Football Analytics and Modeling Experience"</b>, um evento dinâmico destinado a unir a <b>ciência de dados e o futebol</b>. 
O objetivo principal deste evento é criar um ambiente enriquecedor onde alunos, professores e profissionais da indústria do futebol 
possam se conectar, trocar experiências, construir conhecimento e se informar sobre a realidade atual da área de Football Analytics. 
A programação completa do FAME contará com <b>palestras, painéis e apresentação de trabalhos submetidos</b>. A programação do evento ainda será anunciada!

<hr>

### Workshop Pré Evento
- **Data:** 03 de Setembro de 2024
- **Local:** <a href='https://maps.app.goo.gl/DvN4WFp6hKDvHia36'>Centro de Atividades Didáticas 3</a>, UFMG - Campus Pampulha
- **Horário:** 10:00 às 16:00

Visite o <a href="../HandsOn24/">link</a> do workshop e saiba mais.

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



{::nomarkdown}

<script>
function toggleImageBasedOnTheme(is_light) {
    if (is_light) {
        document.getElementById("gemini-logo").src = "../assets/img/FoF/logo_gemini_original.png";
        document.getElementById("onefan-logo").src = "../assets/img/FoF/logo_onefan_original.png";
    } else {
        document.getElementById("gemini-logo").src = "../assets/img/FoF/logo_gemini_branco.png";
        document.getElementById("onefan-logo").src = "../assets/img/FoF/logo_onefan_branco.png";
    }
}
const mode_toggle = document.getElementById("light-toggle");
mode_toggle.addEventListener("click", function() {toggleImageBasedOnTheme(localStorage.getItem("theme") === 'dark');});

document.addEventListener("DOMContentLoaded", toggleImageBasedOnTheme(localStorage.getItem("theme") !== 'dark'));
</script>

{:/nomarkdown}