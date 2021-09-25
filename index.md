---
layout: page
title: "Home"
class: home
---

<div class="columns" markdown="1">

<div class="intro" markdown="1">

I am Linping YUAN (袁林萍), a Ph.D. candidate at [HKUST VisLab](http://vis.cse.ust.hk/), at the Department of Computer Science and Engineering of the [Hong Kong University of Science and Technology (HKUST)](https://hkust.edu.hk/), supervised by Prof. [Huamin Qu](http://www.huamin.org/). Before that, I obtained my bachelor's degree in Software Engineering from [Xi'an Jiaotong University (XJTU)](http://en.xjtu.edu.cn/) in 2019.

My research interests are in Augmented Reality (AR), Human-Computer Interaction (HCI), and Data Visualizations. 

In the first two years of my Ph.D. journey, I focused on how to leverage deep learning methods to facilitate the design of data visualizations and infographics, with an emphasis on color design. I have published two first-author papers on this topic in a top journal.

</div>

<div class="me" markdown="1">
<picture>
  <source srcset='/images/linping_profile.png' type='image/png' />
  <img
    src='/images/linping_profile.png'
    alt='Linping YUAN'>
</picture>

{:.no-list}
<!-- find icons here: https://www.angularjswiki.com/fontawesome/ -->
* <i class="fa fa-envelope"></i> <a href="mailto:{{ site.email }}"> {{ site.email }}</a>
* <i class="fab fa-github"></i> <a href="{{site.github_url}}"> GitHub</a>
* <i class="fab fa-google"></i> <a href="{{site.google_scholar_url}}">Google Scholar</a>
</div>

</div>

<div class="columns" markdown="1"> 
<div class="intro" markdown="1">
Aiming to explore more unknowns and challenge myself, I shifted my interests to AR/VR and have been exploring the intersection of visualization, HCI, and AR/VR since 2020 summer. Currently, I am a core member of [VisLab AR/VR Team](http://vis.cse.ust.hk/groups/xr-vis/). My ongoing research projects aim to build an AR/VR-enhanced campus and enrich HKUST members' living experience with AR/VR techniques and applications.
</div>
</div>

<div class="news" markdown="1">
## Latest News

<table>
<tbody>
{% for news in site.data.news limit:10 %}
  {% include news.html travel=news %}
{% endfor %}
</tbody>
</table>
</div>


## Featured Projects

<div class="featured-projects">
  {% assign sorted_projects = site.data.projects | sort: 'highlight' %}
  {% for project in sorted_projects %}
    {% if project.highlight %}
      {% include project.html project=project %}
    {% endif %}
  {% endfor %}
</div>
<a href="{{ "/projects/" | relative_url }}" class="button">
  <i class="fas fa-chevron-circle-right"></i>
  Show More Projects
</a>

## Featured Publications

<!-- style 1: with border -->
<div class="pubs">
  {% assign sorted_publications = site.publications | sort: 'year' | reverse %}
  {% for pub in sorted_publications %}
    {% if pub.highlight%}
      {% include publication.html pub=pub %}
    {% endif %}
  {% endfor %}
</div>

<!-- style 2: simple; don't delete-->
<!-- <div class="featured-publications">
  {% assign sorted_publications = site.publications | sort: 'year' | reverse %}
  {% for pub in sorted_publications %}
    {% if pub.highlight%}
      <div class="publication pubs">
        {% if pub.doi %}
        <a href="https://doi.org/{{ pub.doi }}" target="_blank"><span class="pub-title">{{ pub.title }}</span>.</a>
        {% elsif pub.pdf %}
        <a href="{{ pub.pdf }}" target="_blank"><span class="pub-title">{{ pub.title }}</span>.</a>
        {% endif %}
        <div class="authors">
          {% for author in pub.authors %}
            {% include person.html person=author %}
            {% unless forloop.last %}, {% endunless %}
          {% endfor %}.
          <br/><i>{{ pub.venue }}</i>, {{ pub.year }}.
          {% if pub.type[0]=="Poster" %} (Poster)
          {% elsif pub.type[0] == "Notes" %} (Notes)
          {% elsif pub.note %} ({{ pub.note }})
          {% endif %}
          {% for award in pub.awards %}
            <br/><span class="award"><i class="fas fa-{% if award == "Best Paper Award" %}trophy{% else %}award{% endif %}" aria-hidden="true"></i> {{ award }}</span>
          {% endfor %}
        </div>
      </div>
    {% endif %}
  {% endfor %}
</div> -->


<a href="{{ "/publications/" | relative_url }}" class="button">
  <i class="fas fa-chevron-circle-right"></i>
  Show All Publications
</a>
