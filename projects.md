---
layout: page
permalink: /projects/
title: Projects
class: projects
---

{:.hidden}

# Projects

{:.lead}
A collection of the projects I have created or contributed significantly to; for work, for fun, or because it needed to be done. Everything listed is open-source and most of the code is found on [GitHub](https://github.com/billyc).

<div class="grid">
  {% for project in site.data.projects %}
    {% include project.html project=project %}
  {% endfor %}
</div>
