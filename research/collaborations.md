---
layout: page
title: Collaborations
permalink: /fr/research/collaborations
lang: fr
submenu: true
---

## Partenaires scientifiques
{% assign strudel_partners = site.data.partners | where: "type", "scientific" %}
<table class='width-100'>
  {% tablerow partner in strudel_partners cols:3 %}
    <div align="center">
      <a href="{{ partner.site }}">
        <b> {{ partner.name }} <br> ({{ partner.longname | capitalize }}) </b>
      </a>
      <br>
      {{ partner.poc }}
    </div>
  {% endtablerow %}
</table>

## Partenaire opérationnels

## Partenaires industriels