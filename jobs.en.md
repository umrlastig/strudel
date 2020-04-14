---
layout: page
title: Jobs
permalink: /en/jobs/
lang: en
---
{% assign strudel_jobs = site.data.recruiting | where: "team", "STRUDEL" %}

{% assign open_jobs = strudel_jobs | where: "filled", "false" %}
{% assign closed_jobs = strudel_jobs | where: "filled", "true" %}

{% assign researchers = open_jobs | where: "type", "EC" %}
{% assign phds = open_jobs | where: "type", "PhD" %}
{% assign internships = open_jobs | where: "type", "Internship" %}

## Teachers / Researchers :

{% for job in researchers %}
  <div>
    <a href="{{ job.pdf_en }}">
      <img src="{{ site.baseurl }}/assets/images/icons/pdf_icon.gif"/>
    </a>
    {{ job.title }}
  </div>
{% endfor %}
{% if researchers.size == 0 %}
  No position available at the moment.
{% endif %}

## Doctorants :

{% for job in phds %}
<div>
  <a href="{{ job.pdf_en }}">
    <img src="{{ site.baseurl }}/assets/images/icons/pdf_icon.gif"/>
  </a>
  {{ job.title }}
</div>
{% endfor %}
{% if phds.size == 0 %}
  No position available at the moment.
{% endif %}

## Stages :

{% for job in internships %}
<div>
  <a href="{{ job.pdf_en }}">
    <img src="{{ site.baseurl }}/assets/images/icons/pdf_icon.gif"/>
  </a>
  {{ job.title }}
</div>
{% endfor %}
{% if internships.size == 0 %}
  No position available at the moment.
{% endif %}
