---
layout: page
permalink: /projekte/
title: Projekte
class: projects
---

{:.hidden}

# Projekte

{:.lead}
Eine Sammlung der Projekte, die ich erstellt oder zu denen ich wesentlich beigetragen habe; für die Arbeit, zum Spaß oder weil es getan werden musste. Alles ist Open-Source und der meiste Code ist auf [GitHub](https://github.com/billyc) zu finden.

<div class="grid">
  {% for project in site.data.projects %}
    {% include project.html project=project %}
  {% endfor %}
</div>
