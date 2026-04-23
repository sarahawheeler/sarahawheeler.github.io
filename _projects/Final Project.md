---
name: Final Project 3.1 - COVID-19
tools: [Python, HTML, vega-lite]
image: assets/pngs/covid.png
description: This is my submission for IS 445's Final Project, an analysis looking at COVID-19 case counts across the world. 
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---
<h3>COVID-19 Case Dashboard:</h3>
<vegachart schema-url="{{ site.baseurl }}/assets/json/dashboard.json" style="width: 100%"></vegachart>
<br>
#<h3>Plot 2:</h3>
#<vegachart schema-url="{{ site.baseurl }}/assets/json/hw6_chart2.json" style="width: 100%"></vegachart>

<br>

<div class="left">
{% include elements/button.html link="https://github.com/sarahawheeler/sarahawheeler.github.io/blob/main/_data/owid-covid-data.csv" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/sarahawheeler/sarahawheeler.github.io/blob/main/python_notebooks/Final_Project_Workbook.ipynb" text="The Analysis" %}
</div>

<br>
<br>
<br>

<h3> Final Project Writeup: </h3>
Group Member Names: Sarah Wheeler

The dashboard I created is a continent-specific look into the COVID-19 pandemic. The top plot in the dashboard displays the fifteen countries in Asia with the highest total case counts (through the end of 2023), aiming to provide the viewer with a quick overview of which countries faced the greatest number of affected people. This plot is intended as the driver, so whenever someone clicks one of the bars in the plot, the two plots below are updates as well. To fully understand trends in case count, we must also look at how it is distributed over time. Thus, the second plot (on the left side of the dashboard, below the bar chart) details cases over time for the entirety of Asia. The orange line, which is updated upon a click to the driver plot (the bar plot), represents that countries new cases trend over time in comparison to the continent as a whole. To isolate each country's contribution to the overall aggregation of continental counts, I created the third plot. Viewers can choose from any Asian country (not just the top 15) to view the overall case number at any point throughout the pandemic via the dropdown. 

When all three plots are examined in combination, I intend for experts and the general public alike to be able to explore how this region of the world was affected by the pandemic, and hope that stark differences in case count for countries that are similar can invite discussion on pandemic management and prevention.

The following are contextual datasets I believe would enrich the quality of the dashboard:

         - World Bank Population Dataset (link: https://data.worldbank.org/indicator/SP.POP.TOTL): This dataset tracks the overall population of each country through the dates the COVID-19 data was collected. One can use this data to normalize the total case count variable to better understand what percentage of a country's population the total_cases statistic amounts to. For example, while China has the highest case count of all Asian countries, it also has one of the highest populations. The population variable in the dataset is stagnant and does not update from day-to-day. I believe that using a variable that is not fixed would allow us to perform normalization at specific time points during the pandemic, providing a more holistic oversight.
         
         - Oxford University's COVID-19 Government Response Tracker (link: https://github.com/OxCGRT/covid-policy-dataset) This dataset describes each country's approach to the pandemic, including many of the measures that were taken and when they were implemented. I would be interested in examining the proactivity of each nation's measures, and comparing that to their normalized case count. Ideally, we'd be able to learn about how the speed of measure implementation can affect success, as well as examine which measures overall proved the most effective in preventing case transmission.
