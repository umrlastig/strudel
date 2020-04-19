# Strudel website

## Presentation of the website

The website contains 6 pages:

- **Jobs**: created automatically from the [recruiting file](https://github.com/umrlastig/lastig_data/recruiting.csv)
- **Members**: created automatically from the [people file](https://github.com/umrlastig/lastig_data/people.csv)
- **Publications**: created automatically using the [HAL open archives API](https://api.archives-ouvertes.fr/docs) and the halIDs (or firstname and lastname if no halID) from the [people file](https://github.com/umrlastig/lastig_data/people.csv)
- **Research**: is a minimalistic description copied from the wiki
- **Projects**: a list of (ongoing and finished) research projects
- **Tools**: a list of research tools developed, used or maintained by the team

## Updating the content of the website

The method depends on the pages:

- for the **Jobs**, **Members**, and **Publications** pages, you should probably directly edit the files on the [LaSTIG data repository](https://github.com/umrlastig/lastig_data/)
- for the **Research** page, directly modify the *research.md* and *research.en.md* files
- for the **Projects** and the **Tools** pages, see the following sections

### Updating the **Projects** page

There are 2 parts to update the **Projects** page:

#### 1. update the *_data/projects.yml* file
A typical entry contains the following

```
- id: landsense
  name: Projet H2020 LandSense
  short_name: LandSense
  start: 2016
  end: 2020
  poc: Laurence Jolivet
  site: https://www.landsense.eu/
  logo: https://eurocrowd.org/wp-content/blogs.dir/sites/85/2016/09/LandSense_logo_big.png
```
Only **id**, **name** and **end** are mandatory.
- **id** is important since it has to match the (lower case) name of the section in the *projects.md* file
- **name** will be used by default in the slider
- **short_name** will be used instead. It is useful when the (full) name if too long for the slider *(optional)*
- **start** start year of the project *(optional)*
- **end** end year of the project. used to separate ongoing projects from terminated ones
- **poc** person of contact for the project *(optional)*
- **site** the website of the project *(optional)*
- **logo** an image that will be used in the slider *(optional)*

#### 2. update the *projects.md* and *projects.en.md* files
A typical entry looks like:

```
<div markdown="1" style="display: block;" id="landsense" class="project">
{% assign project = site.data.projects | where: "id", "landsense" | first %}
## {{project.name}} ({{project.start}} - {{project.end}})

{% if project.title %}
  *{{project.title}}*
  {%- if project.subtitle %}
  <br>*{{project.subtitle}}*
  {% endif %}
{% endif %}

POC : **{{project.poc}}**

{% if project.site %}
  Pour plus d'information, consultez le [site web du projet]({{project.site}})
{% endif %}

</div>
```
- the first and last lines create a *div* enclosing the project description.
  - It is important for the slider to work (it needs something to hide or show).
  - Notice
    - the **style:** is *"display: block;"* for the first project (the one that will be active when the page is loaded) and *"display: none;"* for all the other projects (will be hidden when the page is loaded)
    - the **class:** is *"project"*, which allows the slider to find all the project divs
    - the **id** is *"landsense"*. It has to match a corresponding *id* in the *projects.yml* file
- the rest of the div uses *liquid* to create a default entry with the information in the *projects.yml* file. You can remove/modify all of it or none. That is the place you can add images, text, references, etc.

### Updating the **Tools** page

It is a more simple version of the **Projects** page.
There are 2 parts to update the **Tools** page:

#### 1. update the *_data/tools.yml* file
A typical entry contains the following

```
- id: simplu
  name: SimPLU3D
  logo: https://simplu3d.github.io/logo/logo_small.png
```
Only **id** and **name** are mandatory.
- **id** is important since it has to match the (lower case) name of the section in the *tools.md* file
- **name** will be used by default in the slider
- **short_name** will be used instead. It is useful when the (full) name if too long for the slider *(optional)*
- **logo** an image that will be used in the slider *(optional)*

#### 2. update the *tools.md* and *tools.en.md* files
A typical entry looks like:

```
<div markdown="1" style="display: block;" class="tool-element" id="simplu">

## SimPLU


[Le site web](https://SimPLU3D.github.io).

[SimPLU3D](https://github.com/IGNF/simplu3d), la librairie *java*.

[Tutoriel](https://github.com/SimPLU3D/simplu3D-tutorial).

[Encapsulation pour OpenMOLE](https://github.com/SimPLU3D/simplu3D-openmole).

</div>
```
- the first and last lines create a *div* enclosing the tool description.
  - It is important for the slider to work (it needs something to hide or show).
  - Notice
    - the **style:** is *"display: block;"* for the first project (the one that will be active when the page is loaded) and *"display: none;"* for all the other projects (will be hidden when the page is loaded)
    - the **class:** is *"tool"*, which allows the slider to find all the project divs
    - the **id** is *"simplu"*. It has to match a corresponding *id* in the *tools.yml* file
- the rest of the div is pire Markdown. That is the place you can add images, text, references, etc.
