---
layout: page
title: Projects
permalink: /en/projects/
lang: en
---

Projects lead by {{ site.title.en }} or in which team members are (or were) involved.

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
  For more information, refer to the [project website]({{project.site}}).
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
  For more information, refer to the [project website]({{project.site}}).
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
  For more information, refer to the [project website]({{project.site}}).
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
  For more information, refer to the [project website]({{project.site}}).
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
  For more information, refer to the [project website]({{project.site}}).
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
  For more information, refer to the [project website]({{project.site}}).
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
  For more information, refer to the [project website]({{project.site}}).
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
  For more information, refer to the [project website]({{project.site}}).
{% endif %}

</div>
<br><br>
# Finished projets
{: .post-title}
Links to former projects. Please note some links may be now inactive.<br>

{% include project_bottom_slider.html %}

{% include project_functions.html %}
