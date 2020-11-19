---
layout: page
title: Membres
permalink: /fr/members/
lang: fr
---

{% assign strudel_members = site.data.lastig.people | where: "team", "STRUDEL" %}

{% assign strudel_present_members = strudel_members | where: "member", "true" %}
{% assign strudel_past_members = strudel_members | where: "member", "false" %}

{% assign strudel_permanent_researchers = strudel_present_members | where_exp: "member", "member.status != 'PhD student'" %}

## Permanents :

<table class='width-100'>
  {% tablerow member in strudel_permanent_researchers cols:3 %}
    <div align="center">
      <a href="{{ member.webpage }}">
        <img class="rounded-circle" src="{{ member.photo }}" alt="No image"/>
        <br>
        <b> {{ member.firstname }} <br> {{ member.lastname | capitalize }} </b>
      </a>
      <br>
      {{ member.statut }}
    </div>
  {% endtablerow %}
</table>

{% assign strudel_phds = strudel_present_members | where_exp: "member", "member.status == 'PhD student'" %}

## Doctorants :

<table class='width-100'>
  {% tablerow member in strudel_phds cols:3 %}
    <div align="center">
      <a href="{{ member.webpage }}">
        <img class="rounded-circle" src="{{ member.photo }}" alt="No image"/>
        <br>
        <b> {{ member.firstname }} <br> {{ member.lastname | capitalize }} </b>
      </a>
      <br>
      Depuis {{ member.start_date | split: "/" | last }}
    </div>
  {% endtablerow %}
</table>

## Anciens membres de l'équipe :

<table class='width-100'>
  {% tablerow member in strudel_past_members cols:3 %}
    <div align="center">
      <a href="{{ member.webpage }}">
        <img class="rounded-circle" src="{{ member.photo }}" alt="No image"/>
        <br>
        <b> {{ member.firstname }} <br> {{ member.lastname | capitalize }} </b>
      </a>
      <br>
      {{ member.statut }}
      <br>
      {{ member.start_date | split: "/" | last }} - {{ member.end_date | split: "/" | last }}
    </div>
  {% endtablerow %}
</table>
