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
My first plot visualizes the number of buildings owned/operated by different governmental departments in my home county, with the option to filter by city. I wanted to understand which governmental departments were most present in my home county, and whether different departments spread themselves equally across towns or focused in on specific areas. I used a bar chart with department as a categorical variable on the x-axis and the number of buildings as a quantitative variable on the y-axis. I also used a progressive color theme (“Blues”) that increased the hue of blue based on the height of the column to make more dramatic the differences in number of buildings, as well as to differentiate each department’s column. I did not have to do anything on the data side, aside from filtering the data down only to buildings in my home County.

My second plot is a scatterplot that compares the year constructed and year acquired for buildings acquired by the government in my home county, with the option to filter by floor. I chose to encode the different floors by different colors so we could see visual clusters if they formed. The x-axis represents year constructed and the y-axis represents year acquired, both translated into Datetime format. I used the viridis color palette since it has relatively stark color differences between floors, making it easier to distinguish categories. Because 0 showed up in the data to represent missing values, I dropped these rows and manually adjusted the xlim (while still including all valid data) so that patterns could be shown more easily. This plot is intended to show potential proxies for urbanization and increased government presence in the county.

For both of my graphs, I chose to include interactivity through dropdowns that filter what data is being used in the graph. My first graph allows for filtering by city, which can tell us information about what each city’s role in the overall county may be. For example, Canton (my hometown) is the largest city in the county, so it makes sense that buildings related to higher education and criminality would be there, while smaller agricultural towns like Astoria and Glasford have more buildings belonging to the Department of Natural Resources. Without knowing, much less growing up in, the area, we can still gain insight into its function in the local economy based on which government department owns the greatest proportion of buildings. The interactivity in the second plot, by comparison, gives the reader additional insight into how building characteristics like floor relate to construction and acquisition timing.