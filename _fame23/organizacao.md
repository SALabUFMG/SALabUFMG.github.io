---
layout: team
title: Organização
description: 
img: assets/img/FAME/2022/team-icon.avif
importance: 4
category: work
social: true  # includes social icons at the bottom of the page
---
<hr>
<!-- pages/organizacao.md -->
<div class="team">
    <!-- Display people -->
    {%- assign ordered_people = site.fame23org | sort: "importance" %}
    <!-- Generate cards for each person -->
    <div class="grid">
        {%- for person in ordered_people -%}
            {% include person_card.html %}
        {%- endfor %}
    </div>
    <br>
</div>