---
layout: default
---

Hi there! This is my personal collection of thoughts on topics I find interesting. Most of the time, that means nerding out about urban transport modeling, or data visualization on the web.

### About me

My current research position at [Technische Universität Berlin](https://vsp.tu-berlin.de) focuses on data visualization for the [MATSim transport simulation framework](https://matsim.org). MATSim is currently getting a lot of attention for its ability to simulate traffic scenarios for the impending doomsday arrival of fleets of robot cars.

Formerly I was the Director of Data at the [Puget Sound Regional Council](https://www.psrc.org) in Seattle, Washington. Our team managed all travel forecasting and land use / growth management in support of the Seattle metropolitan region's planning goals.

I am always looking for new interesting projects! Find me on twitter at [@billyinberlin](https://twitter.com/billyinberlin) or on [LinkedIn](https://linkedin.com/in/billy-charlton).

# Recent posts

---

<div class="posts">
  {% for post in site.posts %}
  <div class="post">
    <div class="teaser">
      <h2 class="post-title">
        <a href="{{ site.baseurl }}{{ post.url }}"> {{ post.title }} </a>
      </h2>
    </div>

    <div class="pic-row">
      {% if post.thumbnail %}
      <div class="thumbnail">
        <a href="{{ site.baseurl }}{{ post.url }}">
          <img class="post-thumbnail" src="{{ post.thumbnail }}" />
        </a>
      </div>
      {% endif %}

      <div class="vert-layout">
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
  </div>
  {% endfor %}
</div>
