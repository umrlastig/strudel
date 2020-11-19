---
layout: page
title: Emplois
permalink: /fr/jobs/
lang: fr
---

{% assign strudel_jobs = site.data.lastig.recruiting | where: "team", "STRUDEL" %}

{% assign open_jobs = strudel_jobs | where: "filled", "false" %}
{% assign closed_jobs = strudel_jobs | where: "filled", "true" %}

{% assign researchers = open_jobs | where: "type", "EC" %}
{% assign postdocs = open_jobs | where: "type", "postdoc" %}
{% assign inges = open_jobs | where: "type", "ingenieur" %}
{% assign phds = open_jobs | where: "type", "PhD" %}
{% assign internships = open_jobs | where: "type", "Internship" %}

Vous trouverez ici les offres d'emploi (CDD, CDI) à pourvoir dans l'équipe. Nous vous conseillons vivement de visiter plus en détails ce site et de nous contacter avant de candidater. Merci !

## Enseignants-chercheurs

{% for job in researchers %}
  <div>
    <a href="{{ job.pdf_fr }}">
      <img src="{{ site.baseurl }}/assets/images/icons/pdf_icon.gif"/>
    </a>
    {{ job.titre }}
  </div>
{% else %}
  Aucun poste à pourvoir actuellement.
{% endfor %}

## Post-doctorants

{% for job in postdocs %}
  <div>
    <a href="{{ job.pdf_fr }}">
      <img src="{{ site.baseurl }}/assets/images/icons/pdf_icon.gif"/>
    </a>
    {{ job.titre }}
  </div>
{% else %}
  Aucun poste à pourvoir actuellement.
{% endfor %}

## Ingénieurs

{% for job in inges %}
  <div>
    <a href="{{ job.pdf_fr }}">
      <img src="{{ site.baseurl }}/assets/images/icons/pdf_icon.gif"/>
    </a>
    {{ job.titre }}
  </div>
{% else %}
  Aucun poste à pourvoir actuellement.
{% endfor %}

## Doctorants

{% for job in phds %}
  <div>
    <a href="{{ job.pdf_fr }}">
      <img src="{{ site.baseurl }}/assets/images/icons/pdf_icon.gif"/>
    </a>
    {{ job.titre }}
  </div>
{% else %}
  Aucun poste à pourvoir actuellement.
{% endfor %}

## Stages

{% for job in internships %}
  <div>
    <a href="{{ job.pdf_fr }}">
      <img src="{{ site.baseurl }}/assets/images/icons/pdf_icon.gif"/>
    </a>
    {{ job.titre }}
  </div>
{% else %}
  Aucun poste à pourvoir actuellement.
{% endfor %}
