---
layout: page
title: Publications
permalink: /en/publications/
lang: en
---

{% assign strudel_members = site.data.people | where: "team", "STRUDEL" %}

{% assign strudel_members_HAL = strudel_members | map: "HAL" | uniq | append: "" | join: ", " %}

<script src="{{ site.baseurl }}/assets/js/hal.js" charset="utf-8"></script>

<!-- [ACL] -->
## International Journals
<div id="pubACL"></div>
<!-- to use markdown id naming: {: #pubACL} -->

<!-- [ACLN] -->
## National Journals
<div id="pubACLN"></div>

<!-- [ASCL] -->
## Others
<div id="pubASCL"></div>

<!-- [ACTI] -->
## International Conferences
<div id="pubACTI"></div>

<!-- [ACTN] -->
## National Conferences
<div id="pubACTN"></div>

<!-- [COM] -->
## Communications
<div id="pubCOM"></div>

<!-- [OS] -->
## Book Chapters
<div id="pubOS"></div>

<!-- [DO] -->
## Books
<div id="pubDO"></div>

<!-- [AFF] -->
## Posters
<div id="pubAFF"></div>

<!-- [AP] -->
## Preprints
<div id="pubAP"></div>

<!-- [TH] -->
## Dissertations (PhD theses)
<div id="pubTH"></div>

<!-- [INV] -->
## Invited Talks
<div id="pubINV"></div>

<!-- [PV] -->
## Popularization
<div id="pubPV"></div>

<script defer>
  getPublicationsAuthor({{ strudel_members_HAL }});
</script>
