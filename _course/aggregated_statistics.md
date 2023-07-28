---
layout: page
title: Aggregated Statistics
description: 
img: assets/img/DSAF/estatisticas_agregadas.jpg
importance: 5
category: work
related_publications:
---
<hr>
<br>

<object data="/assets/pdf/CDAF/estatisticas_agregadas.pdf" type="application/pdf" width="900" height="900"></object>

<br>
<br>
<hr>
<br>
You can download the Jupyter notebook below <a href='https://github.com/SALabUFMG/SALabUFMG.github.io/blob/master/assets/jupyter/exercise_2.ipynb'>here</a>

{::nomarkdown}
{% assign jupyter_path = "./assets/jupyter/exercise_2.ipynb" | relative_url %}
{% capture notebook_exists %}{% file_exists ./assets/jupyter/exercise_2.ipynb %}{% endcapture %}
{% if notebook_exists == "true" %}
    {% jupyter_notebook jupyter_path %}
{% else %}
    <p>Sorry, the notebook you are looking for does not exist.</p>
{% endif %}
{:/nomarkdown}