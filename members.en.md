---
layout: page
title: Members
permalink: /en/members/
lang: en
---

{% assign strudel_members = site.data.people | where: "team", "STRUDEL" %}

{% assign strudel_present_members = strudel_members | where: "member", "true" %}
{% assign strudel_past_members = strudel_members | where: "member", "false" %}

{% assign strudel_permanent_researchers = strudel_present_members | where_exp: "member", "member.status != 'PhD student'" %}

## Staff

<table class='width-100'>
  {% tablerow member in strudel_permanent_researchers cols:3 %}
    <div align="center">
      <a href="{{ member.webpage }}">
        <img class="rounded-circle" src="{{ member.photo }}" alt="No image"/>
        <br>
        <b> {{ member.firstname }} <br> {{ member.lastname | capitalize }} </b>
      </a>
      <br>
      {{ member.status }}
    </div>
  {% endtablerow %}
</table>

{% assign strudel_phds = strudel_present_members | where_exp: "member", "member.status == 'PhD student'" %}

## PhD students

<table class='width-100'>
  {% tablerow member in strudel_phds cols:3 %}
    <div align="center">
      <a href="{{ member.webpage }}">
        <img class="rounded-circle" src="{{ member.photo }}" alt="No image"/>
        <br>
        <b> {{ member.firstname }} <br> {{ member.lastname | capitalize }} </b>
      </a>
      <br>
      {{ member.status }}
    </div>
  {% endtablerow %}
</table>

## Alumni

<table class='width-100'>
  {% tablerow member in strudel_past_members cols:3 %}
    <div align="center">
      <a href="{{ member.webpage }}">
        <img class="rounded-circle" src="{{ member.photo }}" alt="No image"/>
        <br>
        <b> {{ member.firstname }} <br> {{ member.lastname | capitalize }} </b>
      </a>
      <br>
      {{ member.status }}
      <br>
      {{ member.start_date | split: "/" | last }} - {{ member.end_date | split: "/" | last }}
    </div>
  {% endtablerow %}
</table>
