---
layout: page
title: Collaborations
permalink: /fr/research/collaborations
lang: fr
submenu: true
---

## Partenaires scientifiques
{% assign strudel_partners_full_sc = site.data.partners | where: "type", "scientific" %}
{% assign strudel_partners_today_sc = strudel_partners_full_sc | where: "end", "false" %}

<table class='width-100'>
  {% tablerow partner in strudel_partners_today_sc cols:4 %}
    <div align="center">
      <a href="{{ partner.site }}">
        <b> {{ partner.name }} <br> ({{ partner.long_name | capitalize }}) </b>
      </a>
      <br>
      <i>{{ partner.poc }}</i>
    </div>
  {% endtablerow %}
</table>

## Partenaire opérationnels

## Partenaires industriels