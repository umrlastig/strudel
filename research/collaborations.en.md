---
layout: page
title: Collaborations
permalink: /en/research/collaborations
lang: en
submenu: true
---

## Academic partners
{% assign strudel_partners_full_sc = site.data.partners | where: "type", "scientific" %}
{% assign strudel_partners_today_sc = strudel_partners_full_sc | where: "end", "false" %}

<table class='width-100'>
  {% tablerow partner in strudel_partners_today_sc cols:4 %}
    <div align="center">
      <a href="{{ partner.site }}">
        <b> {{ partner.name }} <br> ({{ partner.long_name | capitalize }}) </b>
      </a>
     {% if partner.projects %}
		<br> Projet(s): {{ partner.projects }}
		{% endif %}
    </div>
  {% endtablerow %}
</table>

## Operational partners
{% assign strudel_partners_full_op = site.data.partners | where: "type", "operational" %}
{% assign strudel_partners_today_op = strudel_partners_full_op | where: "end", "false" %}

<table class='width-100'>
  {% tablerow partner in strudel_partners_today_op cols:4 %}
    <div align="center">
      <a href="{{ partner.site }}">
        <b> {{ partner.name }} <br> ({{ partner.long_name | capitalize }}) </b>
      </a>
	   {% if partner.projects %}
		<br> Projet(s): {{ partner.projects }}
		{% endif %}
    </div>
  {% endtablerow %}
</table>

## Industrial partners
{% assign strudel_partners_full_indus = site.data.partners | where: "type", "industrial" %}
{% assign strudel_partners_today_indus = strudel_partners_full_indus | where: "end", "false" %}

<table class='width-100'>
  {% tablerow partner in strudel_partners_today_indus cols:4 %}
    <div align="center">
      <a href="{{ partner.site }}">
        <b> {{ partner.name }} <br> ({{ partner.long_name | capitalize }}) </b>
      </a>
	   {% if partner.projects %}
		<br> Projet(s): {{ partner.projects }}
		{% endif %}
    </div>
  {% endtablerow %}
</table>