---
name: HW 6 Plots - Fulton County
tools: [Python, HTML, vega-lite]
image: assets/pngs/fulton_county.png
description: This is my submission for IS 445 HW6, an analysis looking at the building inventory dataset specifically in Fulton County, Illinois.
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---
<h3>Plot 1:</h3>
<vegachart schema-url="{{ site.baseurl }}/assets/json/hw6_chart1.json" style="width: 100%"></vegachart>
<br>
<h3>Plot 2:</h3>
<vegachart schema-url="{{ site.baseurl }}/assets/json/hw6_chart2.json" style="width: 100%"></vegachart>

<br>

<div class="left">
{% include elements/button.html link="https://github.com/sarahawheeler/sarahawheeler.github.io/blob/main/_data/building_inventory.csv" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/sarahawheeler/sarahawheeler.github.io/blob/main/python_notebooks/Workbook.ipynb" text="The Analysis" %}
</div>

<br>
<br>
<br>

<h3> HW 6 Writeup: </h3>
