---
layout: page
title: Emplois
permalink: /fr/jobs/
lang: fr
---

{% assign strudel_jobs = site.data.recruiting | where: "team", "STRUDEL" %}

{% assign open_jobs = strudel_jobs | where: "filled", "false" %}
{% assign closed_jobs = strudel_jobs | where: "filled", "true" %}

{% assign researchers = open_jobs | where: "type", "EC" %}
{% assign phds = open_jobs | where: "type", "PhD" %}
{% assign internships = open_jobs | where: "type", "Internship" %}

## Enseignant-e / Chercheur-se-s :

{% for job in researchers %}
  <div>
    <a href="{{ job.pdf_fr }}">
      <img src="{{ site.baseurl }}/assets/images/icons/pdf_icon.gif"/>
    </a>
    {{ job.titre }}
  </div>
{% endfor %}
{% if researchers.size == 0 %}
  Aucun poste à pourvoir actuellement.
{% endif %}
## Doctorants :

{% for job in phds %}
  <div>
    <a href="{{ job.pdf_fr }}">
      <img src="{{ site.baseurl }}/assets/images/icons/pdf_icon.gif"/>
    </a>
    {{ job.titre }}
  </div>
{% endfor %}
{% if phds.size == 0 %}
  Aucun poste à pourvoir actuellement.
{% endif %}

## Stages :

{% for job in internships %}
  <div>
    <a href="{{ job.pdf_fr }}">
      <img src="{{ site.baseurl }}/assets/images/icons/pdf_icon.gif"/>
    </a>
    {{ job.titre }}
  </div>
{% endfor %}
{% if internships.size == 0 %}
  Aucun poste à pourvoir actuellement.
{% endif %}
