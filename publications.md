---
layout: page
title: Publications
permalink: /fr/publications/
lang: fr
---

{% assign strudel_members = site.data.people | where: "team", "STRUDEL" %}

{% assign strudel_members_HAL = strudel_members | map: "HAL" | uniq | append: "" | join: ", " %}

<script src="{{ site.baseurl }}/assets/js/hal.js" charset="utf-8"></script>

<div id="pubACL">
  [ACL] Journals
</div>

<div id="pubACLN">
  [ACLN] Journals
</div>

<div id="pubASCL">
  [ASCL] Others
</div>

<div id="pubACTI">
  [ACTI] Conferences
</div>

<div id="pubACTN">
  [ACTN] Conferences
</div>

<div id="pubCOM">
  [COM] Conferences
</div>

<div id="pubOS">
  [OS] Books and Chapters
</div>

<div id="pubDO">
  [DO] Books and Chapters
</div>

<div id="pubAFF">
  [AFF] Posters
</div>

<div id="pubAP">
  [AP] Preprints
</div>

<div id="pubTH">
  [TH] Dissertations
</div>

<div id="pubINV">
  [INV] Invited Talks
</div>

<div id="pubPV">
  [PV] Popularization
</div>

<script defer>
  getPublicationsAuthor({{ strudel_members_HAL }});
</script>
