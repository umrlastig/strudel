---
layout: page
title: Membres
permalink: /fr/members/
lang: fr
page_order : 8
---

{% assign strudel_members = site.data.lastig.people | where: "team", "STRUDEL" %}

{% assign strudel_present_members = strudel_members | where: "member", "true" %}
{% assign strudel_past_members = strudel_members | where: "member", "false" %}

{% assign strudel_permanent_researchers = strudel_present_members | where: "perm", "true" %}
{% assign strudel_non_permanent_researchers = strudel_present_members | where: "perm", "false" %}
{% assign strudel_postdocs = strudel_non_permanent_researchers | where_exp: "member", "member.status == 'Post-doc'" %}
{% assign strudel_phds = strudel_non_permanent_researchers | where_exp: "member", "member.status == 'PhD student'" %}
{% assign strudel_engineers = strudel_non_permanent_researchers | where_exp: "member", "member.status == 'Engineer'" %}

## Permanent-e-s :

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

## Post-doctorant-e-s

<table class='width-100'>
  {% tablerow member in strudel_postdocs cols:3 %}
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

## Doctorant-e-s

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

## Ingénieur-e-s

<table class='width-100'>
  {% tablerow member in strudel_engineers cols:3 %}
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

## Anciens membres de l'équipe

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
