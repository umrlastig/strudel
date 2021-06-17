---
layout: page
title: Publications
permalink: /en/publications/
lang: en
page_order : 4
---
<section>
  <ul style="width: 100%; height: 40px; margin: 0; text-align: center; position: relative; overflow-x: auto">
    <li class="tool" onclick="showAllPublications();" style="width: 50%; height: 40px; display: inline-block; position: relative; float: left;">
      <span>All publications</span>
    </li>
    <li class="tool" onclick="showLatestPublications();" style="width: 50%; height: 40px; display: inline-block; position: relative; float: left;">
      <span>Publications of the last 3 years</span>
    </li>
  </ul>
</section>

{% if site.publication_filter %}
  Only the publications of the last {{ site.publication_filter }} years are displayed.
{% endif %}

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
{: #ACL }
<div id="pubACL"></div>
<!-- to use markdown id naming: {: #pubACL} -->

<!-- [ACLN] -->
## {{ site.data.strudel_i18n.ACLN | map: page.lang }}
{: #ACLN }
<div id="pubACLN"></div>

<!-- [ASCL] -->
## {{ site.data.strudel_i18n.ASCL | map: page.lang }}
{: #ASCL }
<div id="pubASCL"></div>

<!-- [ACTI] -->
## {{ site.data.strudel_i18n.ACTI | map: page.lang }}
{: #ACTI }
<div id="pubACTI"></div>

<!-- [ACTN] -->
## {{ site.data.strudel_i18n.ACTN | map: page.lang }}
{: #ACTN }
<div id="pubACTN"></div>

<!-- [COM] -->
## {{ site.data.strudel_i18n.COM | map: page.lang }}
{: #COM }
<div id="pubCOM"></div>

<!-- [OS] -->
## {{ site.data.strudel_i18n.OS | map: page.lang }}
{: #OS }
<div id="pubOS"></div>

<!-- [DO] -->
## {{ site.data.strudel_i18n.DO | map: page.lang }}
{: #DO }
<div id="pubDO"></div>

<!-- [AFF] -->
## {{ site.data.strudel_i18n.AFF | map: page.lang }}
{: #AFF }
<div id="pubAFF"></div>

<!-- [AP] -->
## {{ site.data.strudel_i18n.AP | map: page.lang }}
{: #AP }
<div id="pubAP"></div>

<!-- [TH] -->
## {{ site.data.strudel_i18n.TH | map: page.lang }}
{: #TH }
<div id="pubTH"></div>

<!-- [INV] -->
## {{ site.data.strudel_i18n.INV | map: page.lang }}
{: #INV }
<div id="pubINV"></div>

<!-- [PV] -->
## {{ site.data.strudel_i18n.PV | map: page.lang }}
{: #PV }
<div id="pubPV"></div>

<script>
  function showAllPublications() {
    getPublicationsAuthor({{ clean }});
  }
  function showLatestPublications() {
    var currentYear = new Date().getFullYear()
    var firstYearToDisplay = currentYear - 3
    getPublicationsAuthor({{ clean }}, "["+firstYearToDisplay+" TO "+currentYear+"]");
  }
</script>
<script defer>
{% if site.publication_filter %}
  var currentYear = new Date().getFullYear()
  var firstYearToDisplay = currentYear - parseInt({{ site.publication_filter }})
  getPublicationsAuthor({{ clean }}, "["+firstYearToDisplay+" TO "+currentYear+"]");
{% else %}
  getPublicationsAuthor({{ clean }});
{% endif %}
</script>
