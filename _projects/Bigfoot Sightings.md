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

## Seasonal Bigfoot Sightings by State
<vegachart schema-url="{{ site.baseurl }}/assets/json/chart2.json" style="width: 100%"></vegachart>



## Search The Data & Methods

<div class="left">
{% include elements/button.html link="https://raw.githubusercontent.com/UIUC-iSchool-DataViz/is445_data/main/bfro_reports_fall2022.csv" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/kielsara/kielsara.github.io/blob/main/python_notebooks/HW5-smkiel2.ipynb" text="The Analysis" %}
</div>

