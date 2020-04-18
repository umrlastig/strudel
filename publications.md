---
layout: page
title: Publications
permalink: /fr/publications/
lang: fr
---
{% assign strudel_members = site.data.lastig.people | where: "team", "STRUDEL" %}

{%- capture ids -%}
  {%- for m in strudel_members -%}
    {%- if forloop.first != true -%},{%- endif -%}
    {%- if m.HAL == "todo" -%}
      {%- assign lastname = m.lastname | strip -%}
      authFullName_s:"{{ m.firstname | strip | append: " " | append: lastname | strip | url_encode }}"
    {%- else -%}
      authIdHal_s:{{ m.HAL }}
    {%- endif -%}
  {%- endfor -%}
{%- endcapture -%}
{%- assign clean = ids | strip_newlines | split: "," | append: "" | join: ", " -%}

<script src="{{ site.baseurl }}/assets/js/hal.js" charset="utf-8"></script>

<!-- [ACL] -->
## {{ site.data.strudel_i18n.ACL | map: page.lang }}
<div id="pubACL"></div>
<!-- to use markdown id naming: {: #pubACL} -->

<!-- [ACLN] -->
## {{ site.data.strudel_i18n.ACLN | map: page.lang }}
<div id="pubACLN"></div>

<!-- [ASCL] -->
## {{ site.data.strudel_i18n.ASCL | map: page.lang }}
<div id="pubASCL"></div>

<!-- [ACTI] -->
## {{ site.data.strudel_i18n.ACTI | map: page.lang }}
<div id="pubACTI"></div>

<!-- [ACTN] -->
## {{ site.data.strudel_i18n.ACTN | map: page.lang }}
<div id="pubACTN"></div>

<!-- [COM] -->
## {{ site.data.strudel_i18n.COM | map: page.lang }}
<div id="pubCOM"></div>

<!-- [OS] -->
## {{ site.data.strudel_i18n.OS | map: page.lang }}
<div id="pubOS"></div>

<!-- [DO] -->
## {{ site.data.strudel_i18n.DO | map: page.lang }}
<div id="pubDO"></div>

<!-- [AFF] -->
## {{ site.data.strudel_i18n.AFF | map: page.lang }}
<div id="pubAFF"></div>

<!-- [AP] -->
## {{ site.data.strudel_i18n.AP | map: page.lang }}
<div id="pubAP"></div>

<!-- [TH] -->
## {{ site.data.strudel_i18n.TH | map: page.lang }}
<div id="pubTH"></div>

<!-- [INV] -->
## {{ site.data.strudel_i18n.INV | map: page.lang }}
<div id="pubINV"></div>

<!-- [PV] -->
## {{ site.data.strudel_i18n.PV | map: page.lang }}
<div id="pubPV"></div>

<script defer>
  getPublicationsAuthor({{ clean }});
</script>
