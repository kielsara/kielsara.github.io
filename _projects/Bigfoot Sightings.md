---
name: Bigfoot Sightings Analysis
tools: [Python, HTML, vega-lite, Altair]
image: assets/pngs/bigfoot-sightings.png
description: Practice with Python, Altair, Vegalite
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---

# Visualizing Bigfoot Sightings in The United States

## Total Recorded Bigfoot Sightings by State
<vegachart schema-url="{{ site.baseurl }}/assets/json/chart1.json" style="width: 100%"></vegachart>
This first visualization presents a horizontal bar chart showing the number of reported Bigfoot sightings across different U.S. states. The goal is to highlight the states where these reports are most prevalent. To create this chart, I grouped the dataset by the <code>state</code> column and counted the number of reports associated with each state. Any states with no sightings were dropped from the data. I used a bar encoding for the count, sorted in descending order, with the state names displayed along the y-axis. This simple visual layout allows for quick comparison of sighting frequency by location.

<hr>

## Seasonal Bigfoot Sightings in The United States
<vegachart schema-url="{{ site.baseurl }}/assets/json/chart2.json" style="width: 100%"></vegachart>
The second visualization is an interactive scatter plot map of reported Bigfoot sightings across the United States. Each point on the map represents an individual sighting, with geographic coordinates from the dataset. As with the previous chart, the dataset was grouped by <code>state</code>. I added a dropdown selector that allows users to filter the map based on the season the sighting occurred (Spring, Summer, Fall, or Winter). This was achieved by creating a new <code>season</code> variable derived from the <code>date</code> column and using Altair’s selection object for interactivity. The points are colored by season to visually distinguish patterns, and a tooltip reveals detailed info about each report. This interactive element makes it easier to explore temporal patterns in sightings and provides a more engaging user experience.

<hr>

## Seasonal Bigfoot Sightings by U.S. State
<vegachart schema-url="{{ site.baseurl }}/assets/json/chart3.json" style="width: 100%"></vegachart>

<hr>

## Overall Analysis


<hr>

## Search The Data & Methods

<div class="left">
{% include elements/button.html link="https://raw.githubusercontent.com/UIUC-iSchool-DataViz/is445_data/main/bfro_reports_fall2022.csv" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/kielsara/kielsara.github.io/blob/main/python_notebooks/HW5-smkiel2.ipynb" text="The Analysis" %}
</div>

