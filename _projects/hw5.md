---
name: HW5
tools: [Python, HTML, vega-lite]
image: 
description: 
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---


# Plot 1

The first plot is a bar chart showing the number of bigfoot sightings by state. This is a fairly simple chart that does not require any colormaps because it is just trying to show where in America bigfoot sightings are the most frequent, and a forest green was selected for the chart's color to be thematic to bigfoot. Transformations for this chart were fairly minimal with rows not containing states being dropped. Then the data was grouped by state to sum the total number of sightings per state. Default encodings were selected because they were functional and worked without error.



<vegachart schema-url="{{ site.baseurl }}/assets/json/plot1hw5.json" style="width: 100%"></vegachart>




## Plot 2 

The second plot is a scatter plot mapping bigfoot sightings by year separated by state and colored by season. It also allows for selection of specific seasons or counties to see only the sightings that match these criteria. Season’s were chosen as the colormap to further granularize the date for each data point as well as to see when in the year bigfoot sightings are the most common. Transformations for this chart required the date column to be formatted in a way Altair could understand as well as for any missing data in the season or year columns to be dropped. The seasons dropnas function had to also include sightings labeled as unknown because sightings were labeled with this instead of just being left blank. Allowing users to interactively sort data by county was chosen to allow users to see how many bigfoot sightings have happened in either places they have been or to allow users to understand what type of geography results in increased bigfoot sightings. Seasons were chosen because I felt it to be fairly interesting and allows users to see how bigfoot sightings increase and decrease throughout the year and if all states hold the same trends easily. Default encodings were chosen because they were adequate and fit with the plot minimalist aesthetics.

<vegachart schema-url="{{ site.baseurl }}/assets/json/plot2hw5.json" style="width: 100%"></vegachart>

```
<div class="left">
{% include elements/button.html link="https://github.com/vega/vega/blob/main/docs/data/cars.json" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://blog.4dcu.be/programming/2021/05/03/Interactive-Visualizations.html" text="The Analysis" %}
</div>
```

<!-- these are written in a combo of html and liquid --> 

<div class="left">
{% include elements/button.html link="https://github.com/vega/vega/blob/main/docs/data/cars.json" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/jnaiman/online_cv_public/blob/main/python_notebooks/test_generate_plots.ipynb" text="The Analysis" %}
</div>

