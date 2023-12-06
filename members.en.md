---
layout: page
title: Members
permalink: /en/members/
lang: en
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

## Staff

<table class='width-100'>
  {% tablerow member in strudel_permanent_researchers cols:3 %}
    <div align="center">
      <a href="{{ member.webpage }}">
        <img class="rounded-circle" src="{{ member.photo | default: '/lastig_data/img/abstract-user-icon.svg' }}" alt="No image"/>
        <br>
        <b> {{ member.firstname }} <br> {{ member.lastname | capitalize }} </b>
      </a>
      <br>
      {{ member.status }}
    </div>
  {% endtablerow %}
</table>

## Post-docs

<table class='width-100'>
  {% tablerow member in strudel_postdocs cols:3 %}
    <div align="center">
      <a href="{{ member.webpage }}">
        <img class="rounded-circle" src="{{ member.photo | default: '/lastig_data/img/abstract-user-icon.svg' }}" alt="No image"/>
        <br>
        <b> {{ member.firstname }} <br> {{ member.lastname | capitalize }} </b>
      </a>
      <br>
      Since {{ member.start_date | split: "-" | first }}
    </div>
  {% endtablerow %}
</table>

## PhD students

<table class='width-100'>
  {% tablerow member in strudel_phds cols:3 %}
    <div align="center">
      <a href="{{ member.webpage }}">
        <img class="rounded-circle" src="{{ member.photo | default: '/lastig_data/img/abstract-user-icon.svg' }}" alt="No image"/>
        <br>
        <b> {{ member.firstname }} <br> {{ member.lastname | capitalize }} </b>
      </a>
      <br>
      Since {{ member.start_date | split: "-" | first }}
    </div>
  {% endtablerow %}
</table>

## Engineers

<table class='width-100'>
  {% tablerow member in strudel_engineers cols:3 %}
    <div align="center">
      <a href="{{ member.webpage }}">
        <img class="rounded-circle" src="{{ member.photo | default: '/lastig_data/img/abstract-user-icon.svg' }}" alt="No image"/>
        <br>
        <b> {{ member.firstname }} <br> {{ member.lastname | capitalize }} </b>
      </a>
      <br>
      Since {{ member.start_date | split: "-" | first }}
    </div>
  {% endtablerow %}
</table>

## Alumni

<table class='width-100'>
  {% tablerow member in strudel_past_members cols:3 %}
    <div align="center">
      <a href="{{ member.webpage }}">
        <img class="rounded-circle" src="{{ member.photo | default: '/lastig_data/img/abstract-user-icon.svg' }}" alt="No image"/>
        <br>
        <b> {{ member.firstname }} <br> {{ member.lastname | capitalize }} </b>
      </a>
      <br>
      {{ member.status }}
      <br>
      {{ member.start_date | split: "-" | first }} - {{ member.end_date | split: "-" | first }}
    </div>
  {% endtablerow %}
</table>
