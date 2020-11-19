---
layout: page
title: Jobs
permalink: /en/jobs/
lang: en
page_order : 10
---
{% assign strudel_jobs = site.data.lastig.recruiting | where: "team", "STRUDEL" %}

{% assign open_jobs = strudel_jobs | where: "filled", "false" %}
{% assign closed_jobs = strudel_jobs | where: "filled", "true" %}

{% assign researchers = open_jobs | where: "type", "EC" %}
{% assign postdocs = open_jobs | where: "type", "postdoc" %}
{% assign inges = open_jobs | where: "type", "ingenieur" %}
{% assign phds = open_jobs | where: "type", "PhD" %}
{% assign internships = open_jobs | where: "type", "Internship" %}

You can find here the positions currently available in the team. We highly recommend you to get in touch with us and navigate throughout these fancy pages before applying. Thank you !

## Lecturers

{% for job in researchers %}
  <div>
    <a href="{{ job.pdf_en }}">
      <img src="{{ site.baseurl }}/assets/images/icons/pdf_icon.gif"/>
    </a>
    {{ job.title }}
  </div>
{% else %}
  No position available at the moment.
{% endfor %}

## Post-docs

{% for job in postdocs %}
  <div>
    <a href="{{ job.pdf_fr }}">
      <img src="{{ site.baseurl }}/assets/images/icons/pdf_icon.gif"/>
    </a>
    {{ job.titre }}
  </div>
{% else %}
  No position available at the moment.
{% endfor %}

## Engineers

{% for job in inges %}
  <div>
    <a href="{{ job.pdf_fr }}">
      <img src="{{ site.baseurl }}/assets/images/icons/pdf_icon.gif"/>
    </a>
    {{ job.titre }}
  </div>
{% else %}
  No position available at the moment.
{% endfor %}

## PhD students

{% for job in phds %}
<div>
  <a href="{{ job.pdf_en }}">
    <img src="{{ site.baseurl }}/assets/images/icons/pdf_icon.gif"/>
  </a>
  {{ job.title }}
</div>
{% else %}
  No position available at the moment.
{% endfor %}

## Internships

{% for job in internships %}
<div>
  <a href="{{ job.pdf_en }}">
    <img src="{{ site.baseurl }}/assets/images/icons/pdf_icon.gif"/>
  </a>
  {{ job.title }}
</div>
{% else %}
  No position available at the moment.
{% endfor %}
