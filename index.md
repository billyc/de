---
layout: default
---

Hello! I am a researcher at [Technische Universität Berlin](https://vsp.tu-berlin.de) focusing on data visualization for the [MATSim transport simulation framework](https://matsim.org). MATSim is currently getting a lot of attention for its ability to simulate traffic scenarios for the impending doomsday arrival of fleets of robot cars.

Formerly I was Director of Data for the [Puget Sound Regional Council](https://www.psrc.org) in Seattle, USA. Our 22-person team managed all travel forecasting and land use / growth management in support of the Seattle metropolitan region's planning goals.

### Contact and inquiries

I am always looking for new interesting projects! Find me on twitter at [@billyinberlin](https://twitter.com/billyinberlin) or on [LinkedIn](https://linkedin.com/in/billy-charlton).

# Latest posts

---

<div class="posts">

  {% for post in site.posts %}
  <div class="post">

    <div class="teaser">
      <h2 class="post-title">
        <a href="{{ site.baseurl }}{{ post.url }}"> {{ post.title }} </a>
      </h2>
    </div>

    <div class="index-thumbnail">
      {% if post.thumbnail %}
      <div class="thumbnail">
        <a href="{{ site.baseurl }}{{ post.url }}">
          <img class="post-thumbnail" src="{{ post.thumbnail }}" />
        </a>
      </div>
      {% endif %}
    </div>

    <div class="index-blurb">
      <div class="entry">
        <a class="excerpt" href="{{ site.baseurl }}{{ post.url }}">
          {{ post.excerpt }}
        </a>
      </div>
      <div>
        <a href="{{ site.baseurl }}{{ post.url }}" class="read-more"
          >More&hellip;</a
        >
      </div>
    </div>
  </div>
  {% endfor %}
</div>
