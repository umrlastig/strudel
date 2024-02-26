---
layout: page
title: Publications
permalink: /fr/publications/
lang: fr
page_order : 4
---
<section>
  <ul style="width: 100%; height: 40px; margin: 0; text-align: center; position: relative; overflow-x: auto">
    <li class="tool" onclick="showAllPublications();" style="width: 50%; height: 40px; display: inline-block; position: relative; float: left;">
      <span>Toutes les publications</span>
    </li>
    <li class="tool" onclick="showLatestPublications();" style="width: 50%; height: 40px; display: inline-block; position: relative; float: left;">
      <span>Publications des 3 dernières années</span>
    </li>
  </ul>
</section>

{% if site.publication_filter %}
  Seules les publications des {{ site.publication_filter }} dernières années sont affichées.
{% endif %}

{% assign strudel_members = site.data.lastig.people | where: "team", "STRUDEL" %}

{%- capture ids -%}
  {%- for m in strudel_members -%}
    {%- if forloop.first != true -%},{%- endif -%}
    {%- if m.HAL and m.HAL.size > 0 -%}
      authIdHal_s:{{ m.HAL }}
    {%- else -%}
      {%- assign lastname = m.lastname | strip -%}
      authFullName_s:"{{ m.firstname | strip | append: " " | append: lastname | strip | url_encode }}"
    {%- endif -%}
  {%- endfor -%}
{%- endcapture -%}
{%- assign clean = ids | strip_newlines | split: "," | append: "" | join: ", " -%}

<script src="{{ site.baseurl }}/assets/js/hal.js" charset="utf-8"></script>

<!-- [ACL] -->
<div id="pubACL">
     <h2> {{ site.data.strudel_i18n.ACL | map: page.lang }} </h2>
</div>

<!-- [ACLN] -->
<div id="pubACLN">
     <h2> {{ site.data.strudel_i18n.ACLN | map: page.lang }} </h2>
</div>

<!-- [ASCL] -->
<div id="pubASCL">
     <h2> {{ site.data.strudel_i18n.ASCL | map: page.lang }} </h2>
</div>

<!-- [ACTI] -->
<div id="pubACTI">
     <h2> {{ site.data.strudel_i18n.ACTI | map: page.lang }} </h2>
</div>

<!-- [ACTN] -->
<div id="pubACTN">
     <h2> {{ site.data.strudel_i18n.ACTN | map: page.lang }} </h2>
</div>

<!-- [COM] -->
<div id="pubCOM">
     <h2> {{ site.data.strudel_i18n.COM | map: page.lang }} </h2>
</div>

<!-- [OS] -->
<div id="pubOS">
     <h2> {{ site.data.strudel_i18n.OS | map: page.lang }} </h2>
</div>

<!-- [DO] -->
<div id="pubDO">
     <h2> {{ site.data.strudel_i18n.DO | map: page.lang }} </h2>
</div>

<!-- [AFF] -->
<div id="pubAFF">
     <h2> {{ site.data.strudel_i18n.AFF | map: page.lang }} </h2>
</div>

<!-- [AP] -->
<div id="pubAP">
     <h2> {{ site.data.strudel_i18n.AP | map: page.lang }} </h2>
</div>

<!-- [TH] -->
<div id="pubTH">
     <h2> {{ site.data.strudel_i18n.TH | map: page.lang }} </h2>
</div>

<!-- [INV] -->
<div id="pubINV">
     <h2> {{ site.data.strudel_i18n.INV | map: page.lang }} </h2>
</div>

<!-- [PV] -->
<div id="pubPV">
     <h2> {{ site.data.strudel_i18n.PV | map: page.lang }} </h2>
</div>

<script>
  function showAllPublications() {
    getPublicationsAuthor({{ clean }}, "{{ site.baseurl }}/assets/images");
  }
  function showLatestPublications() {
    var currentYear = new Date().getFullYear()
    var firstYearToDisplay = currentYear - 3
    getPublicationsAuthor({{ clean }}, "{{ site.baseurl }}/assets/images", "["+firstYearToDisplay+" TO "+currentYear+"]");
  }
</script>
<script defer>
{% if site.publication_filter %}
  var currentYear = new Date().getFullYear()
  var firstYearToDisplay = currentYear - parseInt({{ site.publication_filter }})
  getPublicationsAuthor({{ clean }}, "{{ site.baseurl }}/assets/images", "["+firstYearToDisplay+" TO "+currentYear+"]");
{% else %}
  getPublicationsAuthor({{ clean }}, "{{ site.baseurl }}/assets/images");
{% endif %}
</script>
