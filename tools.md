---
layout: page
title: Outils
permalink: /fr/outils/
lang: fr
---
Des outils développés, utilisés ou maintenus par l'équipe.

<section class = "tool-slider">
  <ul class = "tool-slider" id = "slider">
  </ul>
  <div class = "divider">
  </div>
</section>

<div markdown="1" style="display: block;">

## SimPLU

[Le site web](https://SimPLU3D.github.io).

[SimPLU3D](https://github.com/IGNF/simplu3d), la librairie *java*.

[Tutoriel](https://github.com/SimPLU3D/simplu3D-tutorial).

[Encapsulation pour OpenMOLE](https://github.com/SimPLU3D/simplu3D-openmole).

</div>

<div markdown="1" style="display: none;">

## ArtiScales

[Le site web](https://artiscales.github.io/).

[Le code](https://github.com/ArtiScales/).

</div>

<div markdown="1" style="display: none;">

## Librjmcmc

[La bibliothèque libRjmcmc originale](https://github.com/IGNF/librjmcmc), en *C++*.

[librjmcmc4j](https://github.com/IGNF/librjmcmc4j), sa version *java*.

[librjmcmc4s](https://github.com/IGNF/librjmcmc4s), la petite dernière en *scala*.

</div>

<div markdown="1" style="display: none;">

## GeOxygene

[GeOxygene website](https://ignf.github.io/geoxygene/).

[GeOxygene code](https://github.com/IGNF/geoxygene).

[GeOxygene 3D application](https://github.com/IGNF/geoxygene-sig3d-appli).

</div>

<div markdown="1" style="display: none;">

## GeoHistoricalData

### Network matching
[HMMSpatialNetworkMatcher](https://github.com/GeoHistoricalData/HMMSpatialNetworkMatcher).

[nm](https://github.com/GeoHistoricalData/nm).

### Historical Geocoder
[Historical Geocoder](https://github.com/GeoHistoricalData/geocoder-front).

### Arpenteur Topographe
[Le prototype en ligne](https://geohistoricaldata.herokuapp.com/).

[Le code](https://github.com/IGNF/building-inspector).

</div>

<div markdown="1" style="display: none;">

## Autres

### evidence4j

A **Dempster-Shafer** (D-S) engine based on **eVidenZ**, an efficient D-S engine developed in C++ by the *LRDE (Epita Research and Development laboratory)*.

[evidence4j](https://github.com/IGNF/evidence4j) is a *java* library (as its name suggests).

For more information on **eVidenZ**, the original C++ engine, refer to [https://www.lrde.epita.fr/wiki/TheoEvidenz](the eVidenZ webpage).

### NeatMap
[Code](https://github.com/IGNF/NeatMap).

</div>


<script>
  function showTool(toolId) {
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
<script defer>
  var toolsdata = [
    {
      "id": "simplu",
      "logo": "url(https://simplu3d.github.io/logo/logo_small.png)"
    },{
      "id": "librjmcmc",
      "logo": "url(https://raw.githubusercontent.com/IGNF/librjmcmc/master/doc/images/librjmcmc.png)"
    },{
      "id": "geoxygene",
      "logo": "url(http://ignf.github.io/geoxygene/_static/img/geoxygene.png)"
    },{
      "id": "geohistoricaldata",
      "short_name": "GHD",
      "logo": "url(https://avatars0.githubusercontent.com/u/10074559?s=400&u=b6d7f841fe81dad40ccc84d312aed252f7e40b1a&v=4)"
    },{
      "id": "autres",
      "logo": ""
    },{
      "id": "artiscales",
      "logo": "url(https://artiscales.github.io/ArtiScalesExampleSimulationResults.png)"
    }
  ];
  var slider = document.getElementById("slider");
  var tools = document.getElementsByTagName("h2");
  for (i = 0; i < tools.length; i++) {
    var name = tools[i].innerText;
    const id = tools[i].id;
    var li = document.createElement('li');
    li.className = "tool";
    if (i == 0) {li.className += " active";}
    li.style.width = (100 / tools.length)+"%";
    li.setAttribute("toolID", id);
    li.addEventListener('click', event => {
      showTool(id);
    });
    const span = document.createElement('span');
    span.innerHTML = name;
    span.className = "tool-name";
    for (var j = 0 ; j < toolsdata.length ; j++) {
      if (toolsdata[j].id == id) {
        li.style.backgroundImage = toolsdata[j].logo;
        if (toolsdata[j].short_name) {
          span.innerHTML = toolsdata[j].short_name;
        }
      }
    }
    li.appendChild(span);
    slider.appendChild(li);
  }
</script>
