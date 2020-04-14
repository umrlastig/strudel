---
layout: page
title: Membres
permalink: /fr/members/
lang: fr
---

{% assign strudel_members = site.data.people | where: "team", "STRUDEL" %}

{% assign strudel_present_members = strudel_members | where: "member", "true" %}
{% assign strudel_past_members = strudel_members | where: "member", "false" %}

{% assign strudel_permanent_researchers = strudel_present_members | where_exp: "member", "member.status != 'PhD student'" %}

## Permanents :

{% for member in strudel_permanent_researchers %}
  <div>
    <img class="rounded-circle" src="{{ member.photo }}"/>
    <a href="{{ member.webpage }}">
      {{ member.firstname }} {{ member.lastname }}
    </a>
  </div>
{% endfor %}

{% assign strudel_phds = strudel_present_members | where_exp: "member", "member.status == 'PhD student'" %}

## Doctorants :

{% for member in strudel_phds %}
  <div>
    <img class="rounded-circle" src="{{ member.photo }}"/>
    <a href="{{ member.webpage }}">
      {{ member.firstname }} {{ member.lastname }}
    </a>
  </div>
{% endfor %}

## Anciens membres de l'équipe :

{% for member in strudel_past_members %}
  <div>
    <img class="rounded-circle" src="{{ member.photo }}"/>
    <a href="{{ member.webpage }}">
      {{ member.firstname }} {{ member.lastname }}
    </a>
  </div>
{% endfor %}
