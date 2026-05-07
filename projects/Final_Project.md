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
<br>
<h6> Group Member Names: Sarah Wheeler </h6>

<br>
<br>

<h3> Introduction </h3>

The COVID-19 pandemic produced highly uneven transmission outcomes across the globe, with substantial variation in case counts, timing of outbreaks, and overall public health impact. While global aggregates of case counts indeed does provide a broad overview, they often obscure regional differences. It should be noted that this analysis focuses specifically on Asia. Asia presents a compelling case for comparative study due to its diversity in population size, economic development, governance structures, and public health responses. Countries within Asia range from highly populous nations (such as China and India) to smaller states (such as Kuwait) with different healthcare infrastructures and policy approaches. This variation allows for meaningful comparisons within a shared regional context. Additionally, Asia was the initial epicenter of the COVID-19 outbreak, making it important for examining early transmission dynamics. Broadly, this project aims to highlight how different national contexts and response strategies contributed to divergent outcomes within the same geographic region. More specifically, this project is based on the idea that COVID-19 case counts are shaped by both population size and country-specific outbreak timing. Since COVID-19 is an infectious disease, countries with larger populations may naturally report higher total case counts, but population alone may not explain the full pattern. Therefore, this project compares both cumulative case totals and case trends over time to understand whether total cases are mainly a reflection of population size, or whether different outbreak waves and reporting patterns complicate that relationship. The main question is how COVID-19 case patterns differed across Asian countries, and whether those differences can be explained by population-related context or by the timing of different outbreak waves.

<h3> Understanding the Data </h3>

The dataset used in this project is sourced from Our World in Data, which provides a comprehensive, publicly accessible compilation of COVID-19 metrics across countries (Mathieu et al., 2024). The dataset includes daily observations from 2020 through the end of 2023, capturing total confirmed cases, new daily cases, deaths, and vaccination rates. My primary variables of interest are total cases and new cases. Because COVID-19 is an infectious disease, these case numbers are interpreted alongside broader contextual factors, especially population size and population density. Population size matters because countries with more people have a larger possible pool of infections, while population density may affect how easily the virus spreads in crowded urban environments. The Our World in Data dataset also includes population and population density variables, which provide context for interpreting why some countries may report higher or lower case totals. These variables are examined across countries within Asia to identify patterns, peaks, and divergences in case trajectories. It is important to note that the dataset relies on country-level reporting, which may introduce inconsistencies due to differences in testing capacity, reporting standards, and transparency. 

To begin, it is useful to compare total case counts across countries in Asia. The visualization below displays the fifteen countries with the highest cumulative number of COVID-19 cases through the end of 2023. Hovering over a country makes it possible to compare exact case counts, while clicking on a column highlights a specific country for closer comparison. These interactive features are useful because the differences between countries are not only visual, but also numerical and provide distinction.

<vegachart schema-url="{{ site.baseurl }}/assets/json/bar_chart.json" style="width: 100%"></vegachart>

 Nations with large populations, such as China or India, appear prominently, which reflects the relationship between population size and total infections. However, this relationship is not perfectly proportional. Some countries with large population sizes (compared to the rest of the continent) report significantly fewer cases, suggesting that factors beyond population—such as public health interventions, testing capacity, and reporting practices—may have influenced outcomes. One such country is Indonesia. Additionally, while India has the second-highest total case count, when compared to the overall continental trend, its trajectory only mirrors one major surge around April 2022.

 <h3> Contextual Visualizations: Population Size & Density </h3>

Because COVID-19 is an infectious disease, population size is an important context variable for interpreting total case counts. A country with a larger population has a larger possible pool of infections, so comparing raw total cases without considering population can be misleading. The following visualization compares the population sizes of the same high-case Asian countries shown in the first bar chart.

<figure style="text-align: center; margin: 2rem auto; overflow: visible;">
  <img 
    src="/assets/pngs/pop_total.png" 
    alt="Population of the top 15 Asian countries by total COVID-19 cases" 
    style="display: block; width: auto; max-width: 100%; height: auto; margin: 0 auto;"
  >
  <figcaption>Figure: Population of the 15 highest-case Asian countries shown in the total cases bar chart.</figcaption>
</figure>

Population density provides another useful context variable because COVID-19 spreads through close contact. Countries with denser living environments may face different transmission risks than countries where people are more spread out. This visualization compares the population density of the same high-case countries shown in the total cases bar chart.

<figure style="text-align: center; margin: 2rem auto; overflow: visible;">
  <img 
    src="/assets/pngs/pop_dense.png" 
    alt="Population density of the top 15 Asian countries by total COVID-19 cases" 
    style="display: block; width: auto; max-width: 100%; height: auto; margin: 0 auto;"
  >
  <figcaption>Figure: Population density of the same high-case Asian countries shown in the total cases bar chart.</figcaption>
</figure>

<h3> COVID-19 Evolution </h3>

While total case counts provide a useful snapshot, they do not capture how the pandemic evolved. The following time series visualization shows how new COVID-19 cases changed over time across Asia, with the ability to highlight individual countries for comparison. 

<vegachart schema-url="{{ site.baseurl }}/assets/json/asia_overlay.json" style="width: 100%"></vegachart>

 First, the pandemic occurred in multiple waves, with distinct peaks corresponding to different periods of transmission. There are several peaks in April 2022, July 2022, and October 2023 for the whole continent. Different countries contribute considerably differently to this trend. While there is a high similarity between the continental graph and China's graph, the comparison for Iran and Bahrain are vastly different. 

To better understand country-specific dynamics, the following visualization allows for the selection of any Asian country and displays its cumulative case count over time. A singular nation's trends are not always visible when plotted on a scale relative to the continental aggregation. This plot connects the broader regional pattern back to individual countries, making it possible to see whether a country’s total case count developed gradually or through sharp increases. 

<vegachart schema-url="{{ site.baseurl }}/assets/json/country_dropdown.json" style="width: 100%"></vegachart>

Examining trajectories at the country-level highlights a great deal of variation in growth patterns. The timing and magnitude of these waves vary considerably across countries. Some experienced early surges followed by stabilization, while others show delayed or more prolonged increases. Some countries exhibited steady, gradual increases in total cases, while others showed sharp spikes over relatively short periods. In several cases, late-stage surges are evident, indicating that the pandemic’s impact extended well beyond its initial phases. This variation underscores the importance of analyzing both cumulative totals and temporal trends when interpreting COVID-19 data, since two countries may have similar total case counts but very different outbreak histories.

<h3> Conclusion </h3>

Overall, this project shows that COVID-19 case patterns across Asia cannot be explained by total case counts alone. Countries with large populations, such as China and India, often appear prominently in cumulative case comparisons, which suggests that population size is an important context for understanding reported infections. However, the relationship between population and total cases is not perfectly proportional, suggesting that other factors, including public health responses, testing capacity, reporting practices, and outbreak timing, also shaped the data.

The time-based visualizations show that COVID-19 spread across Asia in multiple waves, and that different countries contributed differently to the overall regional pattern. Some countries closely mirrored the continental trend, while others followed very different case trajectories. The key finding is that cumulative totals provide a useful overview, but they can hide major differences in timing, intensity, and country-specific outbreak patterns.

Note: All of the above (both contextual and COVID-19) are original visualizations and their code can be found in the Python notebook linked at the bottom of this page under "The Analysis."

<br>
<h5> References </h5>
Mathieu, E., Ritchie, H., Ortiz-Ospina, E. et al. A global database of COVID-19 vaccinations. Natural Humanities Behavior (2024). https://doi.org/10.1038/s41562-021-01122-8

<br>
<br>
<div class="left">
{% include elements/button.html link="https://github.com/sarahawheeler/sarahawheeler.github.io/blob/main/_data/owid-covid-data.csv" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/sarahawheeler/sarahawheeler.github.io/blob/main/python_notebooks/Final_Project_WB.ipynb" text="The Analysis" %}
</div>