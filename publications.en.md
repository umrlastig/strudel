---
layout: page
title: Publications
permalink: /en/publications/
lang: en
---
{% assign strudel_members = site.data.people | where: "team", "STRUDEL" %}

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
## {{ site.ACL | map: page.lang }}
<div id="pubACL"></div>
<!-- to use markdown id naming: {: #pubACL} -->

<!-- [ACLN] -->
## {{ site.ACLN | map: page.lang }}
<div id="pubACLN"></div>

<!-- [ASCL] -->
## {{ site.ASCL | map: page.lang }}
<div id="pubASCL"></div>

<!-- [ACTI] -->
## {{ site.ACTI | map: page.lang }}
<div id="pubACTI"></div>

<!-- [ACTN] -->
## {{ site.ACTN | map: page.lang }}
<div id="pubACTN"></div>

<!-- [COM] -->
## {{ site.COM | map: page.lang }}
<div id="pubCOM"></div>

<!-- [OS] -->
## {{ site.OS | map: page.lang }}
<div id="pubOS"></div>

<!-- [DO] -->
## {{ site.DO | map: page.lang }}
<div id="pubDO"></div>

<!-- [AFF] -->
## {{ site.AFF | map: page.lang }}
<div id="pubAFF"></div>

<!-- [AP] -->
## {{ site.AP | map: page.lang }}
<div id="pubAP"></div>

<!-- [TH] -->
## {{ site.TH | map: page.lang }}
<div id="pubTH"></div>

<!-- [INV] -->
## {{ site.INV | map: page.lang }}
<div id="pubINV"></div>

<!-- [PV] -->
## {{ site.PV | map: page.lang }}
<div id="pubPV"></div>

<script defer>
  getPublicationsAuthor({{ clean }});
</script>
