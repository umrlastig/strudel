---
layout: page
title: Projets
permalink: /fr/projects/
lang: fr
---
Projets dans lesquels des membres de l'équipe sont impliqués.

<section class = "tool-slider">
  <ul class = "tool-slider" id = "slider">
  {%- for project in site.data.projects -%}
    {%- assign li_width = 100 | divided_by: site.data.projects.size -%}
    <li
    class = "tool{% if project.id == 'landsense' %} active{% endif %}"
    toolID="{{project.id}}"
    onclick="showTool('{{project.id}}');"
    style="width: {{li_width}}%; background-image: url({{project.logo}});">
      <span class="tool-name">
        {{ project.name }}
      </span>
    </li>
  {%- endfor -%}
  </ul>
  <div class = "divider">
  </div>
</section>

<div markdown="1" style="display: block;">

## LandSense

Projet H2020 LandSense(2016-2020)

POC : **Laurence Jolivet**

[Site web](https://www.landsense.eu/)

</div>

<div markdown="1" style="display: none;">

## URCLIM

Projet ERA4CS URCLIM (2017-2020)

POC : **Arnaud Le Bris**

[Site web](http://www.urclim.eu/)

</div>

<div markdown="1" style="display: none;">

## SODUCO

Projet ANR SODUCO (2018 - 2021)

POC : **Julien Perret**

</div>

{% comment %}
Les projets

Projet H2020 LandSense(2016-2020), poc: Laurence Jolivet
Projet ERA4CS URCLIM (2017-2020), poc: Arnaud Le Bris
  http://www.urclim.eu/
Projet ANR SODUCO (2018 - 2021), poc: Julien Perret
SODUCO (ANR, 2019-2023)

Dynamiques Sociales en contexte urbain: outils, modèles et données libres -- Paris et ses banlieues, 1789-1950 (porteur: J. Perret (IGN))


Projet ANR MAESTRIA (2019 - 2022), poc: Clément Mallet
Projet ANR HIATUS (2019 - 2022), poc: Sébastien Giordano
READY3D (2019-2022), poc: Loïc Landrieu
GeoHistoricalData

Projets terminés
  Projet TOSCA PARCELLE (2018 - 2019), poc: Arnaud Le Bris
  BD Constructibilité, collaboration IAUIDF, IGN, DRIEA financée sur fond prorpre
  Projet PEPS UPE PLU++ (2015 - 2016)
    http://ignf.github.io/PLU2PLUS/
{% endcomment %}

<script>
  function showTool(toolId) {
    console.log("Show " + toolId);
    var tools = document.getElementsByTagName("h2");
    for (i = 0; i < tools.length; i++) {
      var id = tools[i].id;
      if (toolId == id) {
        tools[i].parentElement.style.display = "block";
      } else {
        tools[i].parentElement.style.display = "none";
      }
    }
    var toolInSlider = document.getElementById("slider").children;
    for (i = 0; i < toolInSlider.length; i++) {
      var id = toolInSlider[i].getAttribute("toolID");
      if (toolId == id) {
        if (!toolInSlider[i].classList.contains("active")) {
          toolInSlider[i].className += " active";
        }
      } else {
        toolInSlider[i].className = toolInSlider[i].className.replace(" active", "");
      }
    }
  }
</script>
