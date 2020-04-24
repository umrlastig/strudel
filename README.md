# Strudel website

## Presentation of the website

The website contains 6 pages:

- **Jobs**: created automatically from the [recruiting file](https://github.com/umrlastig/lastig_data/recruiting.csv)
- **Members**: created automatically from the [people file](https://github.com/umrlastig/lastig_data/people.csv)
- **Publications**: created automatically using the [HAL open archives API](https://api.archives-ouvertes.fr/docs) and the halIDs (or firstname and lastname if no halID) from the [people file](https://github.com/umrlastig/lastig_data/people.csv)
- **Research**: is a minimalistic description copied from the wiki
- **Projects**: a list of (ongoing and finished) research projects
- **Tools**: a list of research tools developed, used or maintained by the team

## Technical presentation of the website

This is a [jekyll](jekyllrb.com/) website using the [academic](https://github.com/gaalcaras/academic) theme. For an explanation of how a jekyll website is generated, look at the [docs](https://jekyllrb.com/docs/) and [tutorials](https://jekyllrb.com/tutorials/home/).
Specifically, to understand the whole interpretation process, see [this](https://jekyllrb.com/tutorials/orderofinterpretation/).

The repository contains 4 directories, a configuration file (*_config.yml*) and a bunch of *markdown* files.

- **_data**: contains data files (yaml, csv, etc.). See the [datafiles documentation](https://jekyllrb.com/docs/datafiles/) for a detailed explanation.
  In particular, it contains the *projects*, *tools* and other internationalisation files (i18n).
  For instance, the *project.yml* file gives us access to the variable *site.data.projects* containing information about the projects.
  Finally, it also contains le *lastig_data* repository as a git submodule with the name *lastig*.
  That provides us with information on the team members and available jobs.
- **_includes**: contains html files included in differents parts of the site (header, footer, etc.).
- **_posts**: the place you can add news to the website.
- **assets**: contains images, javascript and the style of the site (main*.scss*).

The markdown files in the root directory contains the main pages of the website. Each page has two files, one for the default language (french) and one in english:
- **index.md** (french) and **index.en.md** (english): the home pages of the site
- **jobs.md** (french) and **jobs.en.md** (english): the jobs pages
- **members.md** (french) and **members.en.md** (english): the members pages
- **projects.md** (french) and **projects.en.md** (english): the projects pages
- **publications.md** (french) and **publications.en.md** (english): the publications pages
- **research.md** (french) and **research.en.md** (english): the research pages
- **tools.md** (french) and **tools.en.md** (english): the tools pages

## Updating the content of the website

The method depends on the pages:

- for the **Jobs**, **Members**, and **Publications** pages, you should probably directly edit the files on the [LaSTIG data repository](https://github.com/umrlastig/lastig_data/)
- for the **Projects**, **Tools** and **Research** pages, see the following sections

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

### Presentation
The project has a [website](https://SimPLU3D.github.io).

### Related publications
<div id="simplu"></div>
  <script defer>
    getPublicationsById(["hal-01650530", "tel-02497711", "tel-02525138", "tel-01092212", "hal-02280486", "hal-01650530", "hal-01882706", "hal-01888422", "hal-02176408", "halshs-00776240"], "simplu");
  </script>
</div>

</div>
```
- the first and last lines create a *div* enclosing the tool description.
  - It is important for the slider to work (it needs something to hide or show).
  - Notice
    - the **style:** is *"display: block;"* for the first project (the one that will be active when the page is loaded) and *"display: none;"* for all the other projects (will be hidden when the page is loaded)
    - the **class:** is *"tool"*, which allows the slider to find all the project divs
    - the **id** is *"simplu"*. It has to match a corresponding *id* in the *tools.yml* file
- the rest of the *div* is pure *Markdown*.
  That is the place you can add images, text, references, etc.
- Notice a second *div* with the id *simplu*. This allows to add publications from the *hal API* using the **halIds** of the publications. It uses the javascript method *getPublicationsById*, an array of *halIds* and the id of the sim to add the publications to (*simplu* here).

### Updating the **Research** pages

There is a home research page (*research.md* and *research.en.md*) and subpages in the *research* directory.
The research page is a normal page with a variable *has_submenus: true* that tells us to create a dropdown menu at the top of the site.
Submenus are just pages in the corresponding directory with the variable *submenu: true*.

You can either modify the main page (*research.md* and *research.en.md*) or the subpages (for now only *integration.md* and *integration.en.md*).

## Testing the site locally

If you want to test the site on your machine, follow the following steps:

- In the root Gemfile, add:

```
gem "jekyll", "~> 3.8.5"
```

- and comment the following line:

```
gem "github-pages", group: :jekyll_plugins
```

Please, try not to push these modifications to the repository :wink:

Locally, some images won't show because they use relative urls.
For instance, some images of the members pages refer to images from private pages relative to [the LaSTIG website](https://www.umr-lastig.fr).
