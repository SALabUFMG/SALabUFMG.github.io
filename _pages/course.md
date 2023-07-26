---
layout: page
title: Course
permalink: /dsaf/
description: The home page of the undergraduate course "Data Science Applied to Football", in Portuguese "Ciência de Dados Aplicada ao Futebol", which we first offered in 2023/1.
nav: true
nav_order: 4
horizontal: false
---

<!-- pages/projects.md -->
<hr>

<h3>Data Science Applied to Football</h3>
Welcome to <strong>"Data Science Applied to Football"</strong>, an innovative course uniquely designed to provide a comprehensive understanding of how data science 
techniques can be applied to the world of football. The course draws significant inspiration from the <a href='https://maaikevr.github.io/'>Soccermatics</a> course, but it follows a 
distinct structure, delving into each of the data types in football in each module. They were: <strong>scoresheet data, aggregated statistics, event data, and tracking data</strong>.

Over the span of the course, students had the opportunity to engage with <strong>six different practical exercises</strong>. These exercises were carefully crafted to offer 
hands-on experience with the different data types. <strong>Each exercise was worth 10 points</strong>. However, to encourage learning and progress, the <strong>lowest score 
among the six was discarded</strong>. Unfortunately, due to the timing of the course, tracking data was left out of the practical exercises as students 
were concentrating on their final projects by this point. This part of the course, nonetheless, accounted for <strong>50 points</strong>.

The <strong>final project</strong> was a significant part of this course, carrying the same weight as the practical exercises with <strong>50 points</strong>. 
It wasn't merely about turning in a report. Students were expected to come up with a proposal and make an initial pitch to 
<a href='https://www.linkedin.com/in/rodrigo-picchioni-5154a2a2/'>Rodrigo Picchioni</a> and <a href='https://www.linkedin.com/in/pedro-picchioni-ba959913a/'>Pedro Picchioni</a>. 
This was followed by an intermediate presentation, where students showcased the progress made. In the culmination of the course, students delivered a final presentation 
and a concluding pitch to Rodrigo Picchioni and Pedro Picchioni once again.

The structure of this course, focusing on the practical application of data science to football, offered students an exciting opportunity to 
understand and analyze football from a new, data-driven perspective. With its roots in Soccermatics and its unique structure from data types in 
football, <strong>"Data Science Applied to Football" represents a compelling blend of football knowledge and data science principles</strong>.

<div class="projects">
{%- if site.enable_project_categories and page.display_categories %}
  <!-- Display categorized projects -->
  {%- for category in page.display_categories %}
  <h2 class="category">{{ category }}</h2>
  {%- assign categorized_projects = site.projects | where: "category", category -%}
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
  {%- assign sorted_projects = site.projects | sort: "importance" -%}
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