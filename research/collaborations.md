---
layout: page
title: Collaborations
permalink: /fr/research/collaborations
lang: fr
submenu: true
---

## Partenaires académiques
{% assign strudel_partners_full_sc = site.data.partners | where: "type", "scientific" %}
{% assign strudel_partners_today_sc = strudel_partners_full_sc | where: "end", "false" %}

<table class='width-100'>
  {% tablerow partner in strudel_partners_today_sc cols:3 %}
    <div align="center">
      <a href="{{ partner.site }}">
        {% if partner.logo %}
        <img class="large-logo" src="{{ partner.logo }}" width="40px" alt="No image"/>
        <br>
        {% endif %}
        <b> {{ partner.name }}
		{% if partner.long_name %}
		<br> ({{ partner.long_name | capitalize }})
		{% endif %}
		</b>
      </a>
     {% if partner.projects %}
		<br> Projet(s): {{ partner.projects }}
		{% endif %}
    </div>
  {% endtablerow %}
</table>

## Partenaires opérationnels
{% assign strudel_partners_full_op = site.data.partners | where: "type", "operational" %}
{% assign strudel_partners_today_op = strudel_partners_full_op | where: "end", "false" %}

<table class='width-100'>
  {% tablerow partner in strudel_partners_today_op cols:3 %}
    <div align="center">
      <a href="{{ partner.site }}">
        {% if partner.logo %}
        <img class="large-logo" src="{{ partner.logo }}" alt="No image"/>
        <br>
        {% endif %}
        <b> {{ partner.name }}
		{% if partner.long_name %}
		<br> ({{ partner.long_name | capitalize }})
		{% endif %} </b>
      </a>
	   {% if partner.projects %}
		<br> Projet(s): {{ partner.projects }}
		{% endif %}
    </div>
  {% endtablerow %}
</table>

## Partenaires industriels
{% assign strudel_partners_full_indus = site.data.partners | where: "type", "industrial" %}
{% assign strudel_partners_today_indus = strudel_partners_full_indus | where: "end", "false" %}

<table class='width-100'>
  {% tablerow partner in strudel_partners_today_indus cols:3 %}
    <div align="center">
      <a href="{{ partner.site }}">
        {% if partner.logo %}
        <img class="large-logo" src="{{ partner.logo }}" alt="No image"/>
        <br>
        {% endif %}
        <b> {{ partner.name }}
				{% if partner.long_name %}
		<br> ({{ partner.long_name | capitalize }})
		{% endif %}
		</b>
      </a>
	   {% if partner.projects %}
		<br> Projet(s): {{ partner.projects }}
		{% endif %}
    </div>
  {% endtablerow %}
</table>
