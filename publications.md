---
layout: page
title: Publications
permalink: /fr/publications/
lang: fr
---

{% assign strudel_members = site.data.people | where: "team", "STRUDEL" %}

{% assign strudel_members_HAL = strudel_members | map: "HAL" | uniq | append: "" | join: ", " %}

<script src="{{ site.baseurl }}/assets/js/hal.js" charset="utf-8"></script>

<!-- [ACL] -->
## Journaux internationaux
<div id="pubACL"></div>
<!-- to use markdown id naming: {: #pubACL} -->

<!-- [ACLN] -->
## Journaux nationaux
<div id="pubACLN"></div>

<!-- [ASCL] -->
## Autres
<div id="pubASCL"></div>

<!-- [ACTI] -->
## Conférences internationales
<div id="pubACTI"></div>

<!-- [ACTN] -->
## Conférences nationales
<div id="pubACTN"></div>

<!-- [COM] -->
## Communications
<div id="pubCOM"></div>

<!-- [OS] -->
## Chapitres d'ouvrages
<div id="pubOS"></div>

<!-- [DO] -->
## Directions d'ouvrages
<div id="pubDO"></div>

<!-- [AFF] -->
## Posters
<div id="pubAFF"></div>

<!-- [AP] -->
## Rapports ou pré-publications
<div id="pubAP"></div>

<!-- [TH] -->
## Dissertations (thèses)
<div id="pubTH"></div>

<!-- [INV] -->
## Conférences invitées
<div id="pubINV"></div>

<!-- [PV] -->
## Vulgarisation
<div id="pubPV"></div>

<script defer>
  getPublicationsAuthor({{ strudel_members_HAL }});
</script>
