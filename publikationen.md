---
layout: page
permalink: /publikationen/
title: Publikationen
class: pubs
---

{:.hidden}

# Publications

_Alle Veröffentlichungen erfolgten in englischen Medien. Deswegen sind die folgenden Links nicht ins Deutsche übersetzt._

<div id="facets" class="hidden">
  <div class="facet" id="venue_tags">
    <strong>Venue</strong>
    <ul></ul>
  </div>
  <div class="facet" id="authors">
    <strong>Autoren</strong>
    <ul></ul>
  </div>
  <div class="facet" id="tags">
    <strong>Tag</strong>
    <ul></ul>
  </div>
  <div class="facet" id="type">
    <strong>Art</strong>
    <ul></ul>
  </div>
  <!-- <div class="facet" id="awards">
    <strong>Award</strong>
    <ul></ul>
  </div> -->

</div>

<label id="only-highlight" class="hidden">
  <input type="checkbox" id="highlight">
  Zeig nur Highlights
</label>

<p id="clear-filters" class="hidden">
  <i class="fas fa-times-circle" aria-hidden="true"></i> Clear all filters. <span id="count_hidden">X</span> of <span id="count_total">X</span> publications are hidden by the filters.
</p>

<!-- <input id="ft-search" type="search" placeholder="Search papers..." /> -->

{% assign pubyears = site.publications | group_by:"year"  %}
{% assign sorted_pubyears = pubyears | reverse %}
{% for year in sorted_pubyears %}

## {{ year.name }}

{:#y{{ year.name }} .year}
{% for pub in year.items %}
{% include publication.html pub=pub %}
{% endfor %}
{% endfor %}

<script>
  {% include itemsjs.min.js %}
  {% include pubfilter.js %}
</script>
