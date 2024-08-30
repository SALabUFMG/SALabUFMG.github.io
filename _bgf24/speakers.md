---
layout: team
title: Speakers
description: 
img: assets/img/FAME/2022/presenter-icon.jpeg
importance: 3
category: work
social: false  # includes social icons at the bottom of the page
---
<hr>
<!-- pages/speakers.md -->
<div class="team">
    <!-- Display people -->
    {%- assign ordered_people = site.bgf24pal | sort: "importance" %}
    <!-- Generate cards for each person -->
    <div class="grid">
        {%- for person in ordered_people -%}
            {% include person_card.html %}
        {%- endfor %}
    </div>
    <br>
</div>