---
name: Comparative Patterns of COVID-19 Spread Across Asian Countries
tools: [Python, HTML, vega-lite]
image: assets/pngs/covid.png
description: This is my submission for IS 445's Final Project, an analysis looking at COVID-19 case counts across Asia. 
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---
<h3>Comparative Patterns of COVID-19 Spread Across Asian Countries</h3>
<h6> Group Member Names: Sarah Wheeler </h6>

<br>

<div class="left">
{% include elements/button.html link="https://github.com/sarahawheeler/sarahawheeler.github.io/blob/main/_data/owid-covid-data.csv" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/sarahawheeler/sarahawheeler.github.io/blob/main/python_notebooks/Final_Project_WB.ipynb" text="The Analysis" %}
</div>

<br>
<br>

<h3> Introduction </h3>

The COVID-19 pandemic produced highly uneven outcomes across the globe, with substantial variation in case counts, timing of outbreaks, and overall public health impact. While global aggregates of case counts indeed do provide a broad overview, they often obscure regional differences. It should be noted that this analysis focuses specifically on Asia. Asia presents a compelling case for comparative study due to its diversity in population size, economic development, governance structures, and public health responses. Countries within Asia range from highly populous nations (such as China and India) to smaller states with markedly different healthcare infrastructures and policy approaches. This variation allows for meaningful comparisons within a shared regional context. Additionally, Asia was the initial epicenter of the COVID-19 outbreak, making it important for examining early transmission dynamics. Broadly, this project aims to highlight how different national contexts and response strategies contributed to divergent outcomes within the same geographic region.

<h3> Understanding the Data </h3>

The dataset used in this project is sourced from Our World in Data, which provides a comprehensive, publicly accessible compilation of COVID-19 metrics across countries (Mathieu et al., 2024). The dataset includes daily observations from 2020 through the end of 2023, capturing total confirmed cases, new daily cases, deaths, and vaccination rates. My primary variables of interest are total cases and new cases. These variables are examined across countries within Asia to identify patterns, peaks, and divergences in case trajectories. It is important to note that the dataset relies on country-level reporting, which may introduce inconsistencies due to differences in testing capacity, reporting standards, and transparency. 

To begin, it is useful to compare total case counts across countries in Asia. The visualization below displays the fifteen countries with the highest cumulative number of COVID-19 cases through the end of 2023.

<vegachart schema-url="{{ site.baseurl }}/assets/json/bar_chart.json" style="width: 100%"></vegachart>

 Nations with large populations, such as India, appear prominently, which reflects the relationship between population size and total infections. However, this relationship is not perfectly proportional. Some countries with comparable population sizes report significantly fewer cases, suggesting that factors beyond population—such as public health interventions, testing capacity, and reporting practices—may have influenced outcomes.

While total case counts provide a useful snapshot, they do not capture how the pandemic evolved. The following time series visualization shows how new COVID-19 cases changed over time across Asia, with the ability to highlight individual countries for comparison.

<vegachart schema-url="{{ site.baseurl }}/assets/json/asia_line.json" style="width: 100%"></vegachart>

 First, the pandemic occurred in multiple waves, with distinct peaks corresponding to different periods of transmission. []

To better understand country-specific dynamics, the following visualization allows for the selection of any Asian country and displays its cumulative case count over time.

<vegachart schema-url="{{ site.baseurl }}/assets/json/country_line.json" style="width: 100%"></vegachart>

Examining individual trajectories highlights substantial variation in growth patterns. The timing and magnitude of these waves vary considerably across countries. Some experienced early surges followed by stabilization, while others show delayed or more prolonged increases. Some countries exhibit steady, gradual increases in total cases, while others show sharp spikes over relatively short periods. In several cases, late-stage surges are evident, indicating that the pandemic’s impact extended well beyond its initial phases. This variation underscores the importance of analyzing both cumulative totals and temporal trends when interpreting COVID-19 data.

<br>
<h5> References </h5>
Mathieu, E., Ritchie, H., Ortiz-Ospina, E. et al. A global database of COVID-19 vaccinations. Natural Humanities Behavior (2024). https://doi.org/10.1038/s41562-021-01122-8