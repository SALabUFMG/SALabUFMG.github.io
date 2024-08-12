---
layout: team
title: Palestrantes
description: 
img: assets/img/FAME/2022/presenter-icon.jpeg
importance: 3
category: work
social: true  # includes social icons at the bottom of the page
---
<hr>
<!-- pages/palestrantes.md -->
<div class="team">
    <!-- Display people -->
    {%- assign ordered_people = site.fame24pal | sort: "importance" %}
    <!-- Generate cards for each person -->
    <div class="grid">
        {%- for person in ordered_people -%}
            {% include person_card.html %}
        {%- endfor %}
    </div>
    <br>
</div>