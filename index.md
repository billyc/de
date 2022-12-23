---
layout: page
title: 'Home'
class: home
---

# Hallo, ich bin Billy Charlton

<div class="columns" markdown="1">

<div class="intro" markdown="1">
und ich bin Forscher an der [Technischen Universität Berlin](https://vsp.tu-berlin.de). Ich beschäftige mich mit **Datenvisualisierung** für das [MATSim](https://matsim.org) Verkehrssimulations-Framework.

Bevor ich nach Berlin kam, war ich **Direktor der Datenabteilung** beim [Puget Sound Regional Council](https://www.psrc.org) in Seattle, USA. Wir verwalteten alle Reiseprognosen und die Flächennutzung sowie Wachstumsmanagement zur Unterstützung der Planungsziele der Metropolregion Seattle.

Ich habe einen Master in Bauingenieurwesen am [Northwestern University Transportation Center](https://www.transportation.northwestern.edu/) und einen Bachelor-Abschluss an der [Cornell University](https://www.cee.cornell.edu/cee) erworben.

Ich bin immer auf der Suche nach neuen interessanten Projekten! Schreibt mir bitte eine E-Mail oder findet mich auf Twitter unter @billyinberlin.

</div>

<div class="me" markdown="1">
  <picture>
    <source srcset='{{ "/images/profi-headshot.jpg" | relative_url }}' type='image/jpg' />
    <img
      src='{{ "/images/profi-headshot.jpg" | relative_url }}'
      alt='Billy Charlton'/>
  </picture>

{:.no-list}

- <a href="mailto:{{ site.email }}">{{ site.email }}</a>

</div>

</div>

<!-- During my first year at UW, I received support from the [Fulbright program](https://en.wikipedia.org/wiki/Fulbright_Program). In 2013, I received my B.S. from [Hasso Plattner Institute](https://hpi.de/). I am a scholar of the [German National Academic Foundation](http://www.studienstiftung.de/). I have worked with the [Open Knowledge Foundation](http://www.okfn.org), [Google Research](https://ai.google/research/), and [Microsoft Research](https://www.microsoft.com/en-us/research/group/vibe/). Details are in my [CV]({{ "/cv/" | relative_url }}).
-->

## Ausgewählte Projekte

<div class="featured-projects">
  {% assign sorted_projects = site.data.projects | sort: 'highlight' %}
  {% for project in sorted_projects %}
    {% if project.highlight %}
      {% include project.html project=project %}
    {% endif %}
  {% endfor %}
</div>
<a href="{{ "/projekte/" | relative_url }}" class="button">
  <i class="fas fa-chevron-circle-right"></i>
  Zeig mehr Projekte
</a>

## Ausgewählte Publikationen

<div style="margin-top: -1.2rem; margin-bottom: 1rem;">
<i>Alle Publikationen auf Englisch.</i>
</div>

<div class="featured-publications">
  {% assign sorted_pubs = site.publications | sort: 'highlight' %}
  {% for pub in sorted_pubs %}
    {% if pub.highlight %}
      <a href="{{ pub.pdf }}" class="publication">
        <strong>{{ pub.title }}</strong>
        <span class="authors">{% for author in pub.authors %}{{ author }}{% unless forloop.last %}, {% endunless %}{% endfor %}</span>.
        <i>{{ pub.venue }}, {{ pub.year }}</i>.
        {% for award in pub.awards %}<br/><span class="award"><i class="fas fa-{% if award == "Best Paper Award" %}trophy{% else %}award{% endif %}" aria-hidden="true"></i> {{ award }}</span>{% endfor %}
      </a>
    {% endif %}
  {% endfor %}
</div>

<a href="{{ "/publikationen/" | relative_url }}" class="button">
<i class="fas fa-chevron-circle-right"></i>
Zeig alle Publikationen
</a>

## Aktuelle Blog-Einträge

<div style="margin-top: -1.2rem; margin-bottom: 1rem;">
<i>Der Blog ist auf Englisch.</i>
</div>

<div class="featured-projects">
  {% assign top_posts = site.posts | sort: 'date' | reverse %}
  {% for blog in top_posts limit:3 %}
      {% include blog-blurb.html blog=blog %}
  {% endfor %}
</div>
<a href="{{ "/blog/" | relative_url }}" class="button">
<i class="fas fa-chevron-circle-right"></i>
Zeig alle Beiträge
</a>

<div class="news-travel" markdown="1">

<div class="news" markdown="1">
## Aktuelle Personalien

<ul>
{% for news in site.data.news limit:10 %}
  {% include news.html news=news %}
{% endfor %}
</ul>

</div>

<div class="travel" markdown="1">
## Konferenzen und Reisen

<table>
<tbody>
{% assign future_travel = site.data.travel | where_exp:'item','item.start == null' %}
{% for travel in future_travel %}
  {% include travel.html travel=travel %}
{% endfor %}
{% assign sorted_travel = site.data.travel | where_exp:'item','item.start' | sort: 'start' | reverse %}
{% for travel in sorted_travel limit:10 %}
  {% include travel.html travel=travel %}
{% endfor %}
</tbody>
</table>

</div>

</div>
