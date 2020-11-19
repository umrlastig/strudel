---
layout: page
title: Tools
permalink: /en/tools/
lang: en
page_order : 5
---
The tools used, developed or maintained by the team.
{% include tool_slider.html %}
<script src="{{ site.baseurl }}/assets/js/hal.js" charset="utf-8"></script>

<div markdown="1" style="display: block;" class="tool-element" id="simplu">

## SimPLU

<hr class="tool-header">

![Illustration of SimPLU3D results](https://simplu3d.github.io/img/background/back1.png)

### Presentation

**SimPLU3D** is a set of [Free and Open-Source Java libraries](https://github.com/SimPLU3D/) allowing the *simulation of 3D built configurations* that optimize a numerical utility function under the respect of morphological constraints.
These libraries are used to question the relations between morphological constraints (that may appear in local urban regulation) and the produced urban fabric at the scale of a district or a whole city. The SimPLU3D approach is generic, as it is possible to use customized constraints, utility functions or type of geometric shapes.

![Principe de fonctionnement de SimPLU3D](https://simplu3d.github.io/img/principe.png){:style="height:50%; width:50%; display:block; margin:auto;"}

### Uses

When applied on local urban regulation, this library is notably used to answer to the following questions:

- How many dwellings may be built on a parcel ?
- How may the urban fabric of a district evolve if the local urban regulation is changed ?
- Could the future buildings cause too important shadowing on the neighborhood parcels ?


### More information

All the necessary libraries are available in the [GitHub SimPLU3D organisation](https://github.com/SimPLU3D/) and are developed and maintained by the [STRUDEL team](https://www.umr-lastig.fr/strudel/) of the [LASTIG lab]({{site.url}}) from [IGN](https://www.ign.fr).

For more information, visit the [SimPLU3D website](https://SimPLU3D.github.io).
A [tutorial](https://github.com/SimPLU3D/simplu3D-tutorial) is in particular available to help you set up your own simulations.

![Logo OpenMOLE](https://openmole.org/img/mole/openmole.png){:style="height:50%; width:50%; display:block; margin:auto; background-color: gray; border-radius: 10px; padding: 10px;"}

Finally, SimPLU3D is usable with [OpenMOLE](https://openmole.org) thanks to a [specific OpenMOLE module](https://github.com/SimPLU3D/simplu3D-openmole).

### Bibliography
<div id="simplu"></div>
<script defer>
  getPublicationsById(["hal-01650530", "tel-02497711", "tel-02525138", "tel-01092212", "hal-02280486", "hal-01650530", "hal-01882706", "hal-01888422", "hal-02176408", "halshs-00776240"], "simplu");
</script>
</div>

<div markdown="1" style="display: none;" class="tool-element" id="artiscales">

## ArtiScales
<hr class="tool-header">

The **ArtiScales** simulation platform integrates regional and local planning policies targetting residential development and its regulation.
**ArtiScales** couples 2 models: [MUP-City](https://sourcesup.renater.fr/www/mupcity/) and [SimPLU3D](https://simplu3d.github.io/).

![Illustration of an ArtiScales simulation result](https://artiscales.github.io/ArtiScalesExampleSimulationResults.png){:style="height:100%; width:100%; display:block; margin:auto;"}

### More information

These libraries are available on the [ArtiScales GitHub organisation](https://github.com/ArtiScales/) and are developped and maintained by [Maxime Colomb](http://maxime-colomb.eu/) with the help of the [STRUDEL team](https://www.umr-lastig.fr/strudel/) of the [LASTIG lab]({{site.url}}) from [IGN](https://www.ign.fr).

For more information, visit the [ArtiScales website](https://artiscales.github.io/).

![Logo OpenMOLE](https://openmole.org/img/mole/openmole.png){:style="height:50%; width:50%; display:block; margin:auto; background-color: gray; border-radius: 10px; padding: 10px;"}

Finally, ArtiScales can be used in distributed environnements thanks to [OpenMOLE](https://openmole.org) and the [OpenMOLE module](https://github.com/ArtiScales/Artiscales-openmole).

### Bibliography
<div id="artiscales"></div>
<script defer>
  getPublicationsById(["tel-02497711"], "artiscales");
</script>
</div>

<div markdown="1" style="display: none;" class="tool-element" id="librjmcmc">

## Librjmcmc


[The original libRjmcmc library](https://github.com/IGNF/librjmcmc), written in *C++*.

[librjmcmc4j](https://github.com/IGNF/librjmcmc4j), its *java* version.

[librjmcmc4s](https://github.com/IGNF/librjmcmc4s), its *scala* version.

</div>

<div markdown="1" style="display: none;" class="tool-element" id="geoxygene">

## GeOxygene


[GeOxygene website](https://ignf.github.io/geoxygene/).

[GeOxygene code](https://github.com/IGNF/geoxygene).

[GeOxygene 3D application](https://github.com/IGNF/geoxygene-sig3d-appli).

</div>

<div markdown="1" style="display: none;" class="tool-element" id="geohistoricaldata">

## GeoHistoricalData


### Network matching

[HMMSpatialNetworkMatcher](https://github.com/GeoHistoricalData/HMMSpatialNetworkMatcher).

[nm](https://github.com/GeoHistoricalData/nm).

### Historical Geocoder

[Historical Geocoder](https://github.com/GeoHistoricalData/geocoder-front).

### Arpenteur Topographe

[An online prototype](https://geohistoricaldata.herokuapp.com/).

[Its code](https://github.com/IGNF/building-inspector).

</div>


<div markdown="1" style="display: none;" class="tool-element" id="openmole">

## OpenMOLE


<hr class="tool-header">


![Logo OpenMOLE](https://openmole.org/img/mole/openmole.png){:style="height:50%; width:50%; display:block; margin:auto; background-color: gray; border-radius: 10px; padding: 10px;"}

### Presentation

[OpenMOLE](https://next.openmole.org/) is a free and open-source platform devoted to simulation model exploration, developed at the Complex System  Institute of Paris ([ISC-PIF](https://iscpif.fr/)). It offers tools to run, explore, diagnose and optimize your numerical model, taking advantage of distributed computing environments. OpenMOLE offers to embed your already developed model, in any language (Java, Binary exe, NetLogo, R, SciLab, Python, C++...).

### Uses

OpenMOLE methods allows to perform various kind of Design of Experiments (DoE) : real sensitivity analysis, calibration on mono/multi criterion, pattern diversity research in model dynamics, custom design of experiments, data processing....


### More information

[OpenMOLE website](https://next.openmole.org/)

[community chat](https://chat.openmole.org/)

[code repository](https://gitlab.openmole.org/openmole)

[twitter account](https://twitter.com/OpenMOLE)




### Bibliography

STRUDEL team papers featuring the use of OpenMOLE

<div id="openmole"></div>
<script defer>
  getPublicationsById(["hal-01650530", "tel-02497711", "tel-02525138", "tel-01092212",], "openmole");
</script>
</div>


<div markdown="1" style="display: none;" class="tool-element" id="autres">

## Autres


### evidence4j

A **Dempster-Shafer** (D-S) engine based on **eVidenZ**, an efficient D-S engine developed in C++ by the *LRDE (Epita Research and Development laboratory)*.

[evidence4j](https://github.com/IGNF/evidence4j) is a *java* library (as its name suggests).

For more information on **eVidenZ**, the original C++ engine, refer to [the eVidenZ webpage](https://www.lrde.epita.fr/wiki/TheoEvidenz).

### NeatMap
[Code](https://github.com/IGNF/NeatMap).

</div>






{% include tool_functions.html %}
