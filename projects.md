---
layout: page
title: Projets
permalink: /fr/projects/
lang: fr
page_order : 6
---
Projets pilotés par STRUDEL ou dans lesquels des membres de l'équipe sont impliqués.

{% include project_slider.html %}

<div markdown="1" style="display: block;" id="landsense" class="project">
{% assign project = site.data.projects | where: "id", "landsense" | first %}
## {{project.name}} ({{project.start}} - {{project.end}})

{% if project.title %}
  *{{project.title}}*
  {%- if project.subtitle %}
  <br>*{{project.subtitle}}*
  {% endif %}
{% endif %}

PI/POC : **{{project.poc}}**

{% if project.site %}
  Pour plus d'information, consultez le [site web du projet]({{project.site}}).
{% endif %}

</div>

<div markdown="1" style="display: none;" id="urclim" class="project">
{% assign project = site.data.projects | where: "id", "urclim" | first %}

## {{project.name}} ({{project.start}} - {{project.end}})

{% if project.title %}
  *{{project.title}}*
  {% if project.subtitle %}
  *{{project.subtitle}}*
  {% endif %}
{% endif %}

PI/POC : **{{project.poc}}**

{% if project.site %}
  Pour plus d'information, consultez le [site web du projet]({{project.site}}).
{% endif %}

</div>

<div markdown="1" style="display: none;" id="soduco" class="project">
{% assign project = site.data.projects | where: "id", "soduco" | first %}
## {{project.name}} ({{project.start}} - {{project.end}})

{% if project.title %}
  *{{project.title}}*
  {%- if project.subtitle %}
  <br>*{{project.subtitle}}*
  {% endif %}
{% endif %}

PI/POC : **{{project.poc}}**

{% if project.site %}
  Pour plus d'information, consultez le [site web du projet]({{project.site}}).
{% endif %}

</div>

<div markdown="1" style="display: none;" id="maestria" class="project">
{% assign project = site.data.projects | where: "id", "maestria" | first %}

## {{project.name}} ({{project.start}} - {{project.end}})

{% if project.title %}
  *{{project.title}}*
  {%- if project.subtitle %}
  <br>*{{project.subtitle}}*
  {% endif %}
{% endif %}

PI/POC : **{{project.poc}}**

{% if project.site %}
  Pour plus d'information, consultez le [site web du projet]({{project.site}}).
{% endif %}

</div>

<div markdown="1" style="display: none;" id="hiatus" class="project">
{% assign project = site.data.projects | where: "id", "hiatus" | first %}

## {{project.name}} ({{project.start}} - {{project.end}})

{% if project.title %}
  *{{project.title}}*
  {% if project.subtitle %}
  *{{project.subtitle}}*
  {% endif %}
{% endif %}

PI/POC : **{{project.poc}}**

{% if project.site %}
  Pour plus d'information, consultez le [site web du projet]({{project.site}}).
{% endif %}

</div>

<div markdown="1" style="display: none;" id="ready3d" class="project">
{% assign project = site.data.projects | where: "id", "ready3d" | first %}

## {{project.name}} ({{project.start}} - {{project.end}})

{% if project.title %}
  *{{project.title}}*
  {% if project.subtitle %}
  *{{project.subtitle}}*
  {% endif %}
{% endif %}

PI/POC : **{{project.poc}}**

{% if project.site %}
  Pour plus d'information, consultez le [site web du projet]({{project.site}}).
{% endif %}

</div>

<div markdown="1" style="display: none;" id="tosca" class="project">
{% assign project = site.data.projects | where: "id", "tosca" | first %}

## {{project.name}} ({{project.start}} - {{project.end}})
{% if project.title %}
  *{{project.title}}*
  {% if project.subtitle %}
  *{{project.subtitle}}*
  {% endif %}
{% endif %}

PI/POC : **{{project.poc}}**

{% if project.site %}
  Pour plus d'information, consultez le [site web du projet]({{project.site}}).
{% endif %}

</div>

<div markdown="1" style="display: none;" id="plu2plus" class="project">
{% assign project = site.data.projects | where: "id", "plu2plus" | first %}

## {{project.name}} ({{project.start}} - {{project.end}})
{% if project.title %}
  *{{project.title}}*
  {% if project.subtitle %}
  *{{project.subtitle}}*
  {% endif %}
{% endif %}

PI/POC : **{{project.poc}}**

{% if project.site %}
  Pour plus d'information, consultez le [site web du projet]({{project.site}}).
{% endif %}

</div>
<br><br>
# Projets terminés
{: .post-title}
Des liens vers des anciens projets. Vous comprendrez que certains liens puissent ne plus être actifs.<br>

{% include project_bottom_slider.html %}

{% include project_functions.html %}
