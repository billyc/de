---
title: Creating and visualizing a model of all traffic in Switzerland
layout: post
thumbnail: /images/2020/snf-swiss-simulation-thumb.jpg
---

At TU Berlin, we are building a MATSim transport simulation model of all trips occurring within the nation of Switzerland. Our goal: build a full national model *only from easily-obtainable data sources* such as census and aggregate mobile phone data. So, is it possible?

### Yes!

**Click on the image below** to open a live animation of a 1% sample of 8 A.M. traffic. Be patient, this will take some time to load. The dataset is quite large!!

<a href="https://vsp-snf.surge.sh" target="_blank">
![Swiss Traffic](/images/2020/snf-swiss-simulation.jpg)
</a>

To build a MATSim model, the two key inputs needed are a depiction of the transport system (i.e. the roadway network and transit routes and services) and the activity patterns of the population.

- The networks can be generated from publicly available data sources such as [OpenStreetMap]() and [GTFS](). For this study we used OSM-derived networks created at ETH Zurich.
- But the activity patterns are usually more difficult to create without specialized datasets such as regional travel surveys.

Our approach was to use the Swiss Census to identify the home locations of the population, and aggregate summaries from the SwissCom mobile phone provider for estimating a matrix of municipality-to-municipality commute patterns. Much more detail will be forthcoming in the project final report.


### Comparison to existing simulation model

ETH Zurich has a very detailed model of Switzerland already in operation. How different are these models?

- The ETH model includes freight, which we have not addressed thus far
- The ETH model is fully calibrated based on existing traffic counts and other measures

After removing freight trips so the models are comparable, our simplified model had about 4.5 percent fewer activities. Since both models use census data for home locations, and since the work locations are coming from the mobile phone data, we decided to take a closer look at the other activities: nonwork trips such as social, recreational, and shopping trips for which we had less data.

Some differences are visible in the side-by-side comparison:

![Non-work activity locations](/images/2020/snf-secondary-activities-comparison.png)

We will be looking into this in more detail as the project continues. Lots of fun stuff to sink our teeth into!

### Afterword

The research described here is a proof of concept, not a fully-calibrated tool ready for planning or decisionmaking. With further development, this approach could be considered one of the most cost-effective and simple methods of generating a usable MATSim scenario for many different regions.


This work is sponsored by the [Swiss National Science Foundation](http://www.snf.ch/en/Pages/default.aspx) and performed by researchers at [TU Berlin](https://vsp.tu-berlin.de).
