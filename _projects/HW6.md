---
name: Experimenting with Jekyll
tools: [Python, HTML, vega-lite]
image: assets/pngs/cars.png
description: This is my submission for IS 445 HW6!
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---


<vegachart schema-url="{{ site.baseurl }}/assets/json/cars.json" style="width: 100%"></vegachart>

<div class="left">
{% include elements/button.html link="https://github.com/vega/vega/blob/main/docs/data/cars.json" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/jnaiman/online_cv_public/blob/main/python_notebooks/test_generate_plots.ipynb" text="The Analysis" %}
</div>

