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
This first visualization presents a horizontal bar chart showing the number of reported Bigfoot sightings across different U.S. states. The goal is to highlight the states where these reports are most prevalent. To create this chart, I grouped the dataset by the <code>state</code> column and counted the number of reports associated with each state. Any states with no sightings were dropped from the data. I used a bar encoding for the count, sorted in descending order, with the state names displayed along the y-axis. This simple visual allows for quick comparison of sighting frequency by location.

<hr>

## Seasonal Bigfoot Sightings in The United States
<vegachart schema-url="{{ site.baseurl }}/assets/json/chart2.json" style="width: 100%"></vegachart>
The second visualization is an interactive scatter plot map of reported Bigfoot sightings across the United States. Each point on the map represents an individual sighting, with geographic coordinates from the dataset. As with the previous chart, the dataset was grouped by <code>state</code>. I added a dropdown selector that allows users to filter the map based on the season the sighting occurred (Spring, Summer, Fall, or Winter). This was achieved by creating a new <code>season</code> variable derived from the <code>date</code> column and using Altair’s selection object for interactivity. The points are colored by season - with typical colors associated with each season - to visually distinguish patterns, and a tooltip reveals detailed info about each report. This interactive element makes it easier to explore time-related patterns in sightings.

<hr>

## Seasonal Bigfoot Sightings by U.S. State
<vegachart schema-url="{{ site.baseurl }}/assets/json/chart3.json" style="width: 100%"></vegachart>
The third and final visualization combines elements of the previous two charts to provide a more focused exploration of Bigfoot sightings by both state and season. Users can select a season from a dropdown menu to highlight seasonal patterns, and choose a specific state to only show sightings that occured within the selected state. This layout helps users explore both national trends and localized patterns in reported Bigfoot encounters, in addition to the time-related aspect of exploring by season.

<hr>

## Overall Analysis
Bigfoot is most commonly associated with being a creature of the Pacific Northwest, which includes Washington and Oregon. It makes sense then that these two states are in the top 5 of states with Bigfoot sightings and have a large amount of sightings visually grouped together on the two maps. There does not seem to be too much of a correlation between sightings and seasons, at least based on visual cues given from the last two charts.

<hr>

## Search The Data & Methods

<div style="display: flex; gap: 1rem;">
  <div>
    {% include elements/button.html link="https://raw.githubusercontent.com/UIUC-iSchool-DataViz/is445_data/main/bfro_reports_fall2022.csv" text="The Data" %}
  </div>
  <div>
    {% include elements/button.html link="https://github.com/kielsara/kielsara.github.io/blob/main/python_notebooks/HW5-smkiel2.ipynb" text="The Analysis" %}
  </div>
</div>
