---
layout: page
title: Outils
permalink: /fr/outils/
lang: fr
---
Des outils développés, utilisés ou maintenus par l'équipe.
{% include tool_slider.html %}
<script src="{{ site.baseurl }}/assets/js/hal.js" charset="utf-8"></script>

<div markdown="1" style="display: block;" class="tool-element" id="simplu">

## SimPLU

<hr class="tool-header">

![Illustration de résultats de SimPLU3D](https://simplu3d.github.io/img/background/back1.png)

### Présentation

**SimPLU3D** est un ensemble de [bibliothèques Java libres et Open-Source](https://github.com/SimPLU3D/) qui permet de *simuler des formes bâties 3D* à partir de contraintes morphologiques en optimisant une fonction numérique.
Ces codes peuvent être utilisés pour questionner le rapport entre des contraintes morphologiques (par exemple, issues de réglementations locales d'urbanisme) et les formes produites à l'échelle du quartier ou de l'agglomération. L'approche de SimPLU3D est générique dans le sens où il est possible de définir ses propres contraintes, fonctions d'optimisation ou types de formes.

![Principe de fonctionnement de SimPLU3D](https://simplu3d.github.io/img/principe.png){:style="height:50%; width:50%; display:block; margin:auto;"}

### Utilisations

Cette bibliothèque a notamment été utilisée pour modéliser des formes bâties à partir de contraintes issues de Plans Locaux d'Urbanisme (PLU) et permet de répondre à ce type de questions :

- Quelle est la quantité maximale de logements que l'on peut bâtir sur une parcelle ?
- Comment la forme de mon quartier va évoluer si l'on modifie un PLU ?
- Est-ce que des bâtiments produisant une ombre trop importante sur les parcelles voisines risquent d'être construits ?

### Plus d'information

L'ensemble de ces bibliothèques est disponible dans l'[organisation GitHub SimPLU3D](https://github.com/SimPLU3D/) et est développé et maintenu par l'[équipe STRUDEL](https://www.umr-lastig.fr/strudel/) du [laboratoire LASTIG]({{site.url}}) de l'[Institut National de l'Information Géographique et Forestière](https://www.ign.fr).

Pour plus d'information, visitez [le site web de SimPLU3D](https://SimPLU3D.github.io).
Un [tutoriel](https://github.com/SimPLU3D/simplu3D-tutorial) est en particulier disponible pour faire vos propres simulations.

![Logo OpenMOLE](https://openmole.org/img/mole/openmole.png){:style="height:50%; width:50%; display:block; margin:auto; background-color: gray; border-radius: 10px; padding: 10px;"}

Enfin, SimPLU3D est utilisable dans des environnement de calcul distribués et peut notamment être utilisé avec [OpenMOLE](https://openmole.org) grâce à une [encapsulation pour OpenMOLE](https://github.com/SimPLU3D/simplu3D-openmole).

### Références bibliographiques
<div id="simplu"></div>
<script defer>
  getPublicationsById(["hal-01650530", "tel-02497711", "tel-02525138", "tel-01092212", "hal-02280486", "hal-01650530", "hal-01882706", "hal-01888422", "hal-02176408", "halshs-00776240"], "simplu");
</script>
</div>

<div markdown="1" style="display: none;" class="tool-element" id="artiscales">

## ArtiScales

<hr class="tool-header">

La plate-forme de simulation **ArtiScales** permet d'intégrer les politiques d'aménagement régionales et locales qui visent à réguler le développement résidentiel. **ArtiScales** couple 2 modèles : [MUP-City](https://sourcesup.renater.fr/www/mupcity/) et [SimPLU3D](https://simplu3d.github.io/).

![Illustration d'un résultat de simulation d'ArtiScales](https://artiscales.github.io/ArtiScalesExampleSimulationResults.png){:style="height:100%; width:100%; display:block; margin:auto;"}

### Plus d'information

L'ensemble de ces bibliothèques est disponible dans l'[organisation GitHub ArtiScales](https://github.com/ArtiScales/) et est développé et maintenu par [Maxime Colomb](http://maxime-colomb.eu/) avec l'aide de l'[équipe STRUDEL](https://www.umr-lastig.fr/strudel/) du [laboratoire LASTIG]({{site.url}}) de l'[Institut National de l'Information Géographique et Forestière](https://www.ign.fr).

Pour plus d'information, visitez [le site web d'ArtiScales](https://artiscales.github.io/).

![Logo OpenMOLE](https://openmole.org/img/mole/openmole.png){:style="height:50%; width:50%; display:block; margin:auto; background-color: gray; border-radius: 10px; padding: 10px;"}

Enfin, ArtiScales est utilisable dans des environnement de calcul distribués et peut notamment être utilisé avec [OpenMOLE](https://openmole.org) grâce à une [encapsulation pour OpenMOLE](https://github.com/ArtiScales/Artiscales-openmole).

### Références bibliographiques
<div id="artiscales"></div>
<script defer>
  getPublicationsById(["tel-02497711"], "artiscales");
</script>
</div>

<div markdown="1" style="display: none;" class="tool-element" id="librjmcmc">

## Librjmcmc


[La bibliothèque libRjmcmc originale](https://github.com/IGNF/librjmcmc), en *C++*.

[librjmcmc4j](https://github.com/IGNF/librjmcmc4j), sa version *java*.

[librjmcmc4s](https://github.com/IGNF/librjmcmc4s), la petite dernière en *scala*.

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

[Le prototype en ligne](https://geohistoricaldata.herokuapp.com/).

[Le code](https://github.com/IGNF/building-inspector).

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
