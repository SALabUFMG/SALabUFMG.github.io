---
layout: page
title: The Business of Global Football '24 (1<sup>st</sup> Edition)
permalink: /BGF24/
description:
nav: false
nav_order: 
horizontal: false
social: false  # includes social icons at the bottom of the page
---

<!-- pages/bgf24.md -->

### Sponsorship
Sponsored by: <br/>
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

Be a part of our extraordinary event and showcase your brand's commitment to excellence.
<a href='../sponsorship/'>Click here</a> to explore our exclusive sponsorship packages and discover how we can create a tailored partnership that aligns with your goals.
<hr>

### Tickets
Get your tickets now for this amazing event! <a href='https://www.sympla.com.br/evento/future-of-football-conference-fame-24-business-of-global-football-ufmg-nyu/2559817'>Click here</a> to purchase your tickets and secure your spot.

<hr>

### About the event
- **Date:** September 04, 2024
- **Local:** <a href='https://maps.app.goo.gl/DvN4WFp6hKDvHia36'>Centro de Atividades Didáticas 3</a>, UFMG - Campus Pampulha
- **Hour:** 12:00pm to 6:30pm

<hr>

<div class="projects">
{%- if site.enable_project_categories and page.display_categories %}
  <!-- Display categorized projects -->
  {%- for category in page.display_categories %}
  <h2 class="category">{{ category }}</h2>
  {%- assign categorized_projects = site.bgf24 | where: "category", category -%}
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
  {%- assign sorted_projects = site.bgf24 | sort: "importance" -%}
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