---
title: Flood Event Analysis
categories:
- General
feature_image: "https://picsum.photos/2560/600?image=872"
---

The Front Range Flood Event was a significant flood in Northern Colorado that occured in September, 2013.

## Data Choice
My first experience fully understanding the effects of floods, was when this event occured. We took a field trip to Loveland, CO to look at the damage. A park I used to go to when I was young was under 10 feet of debris. I wanted to analyze this flood, and see how likely it is to happen again. I found a gage location near that park to analyze the stream discharge data in order to understand the return year and probability.

<iframe src="/assets/flood-analysis/gauge-location.html"
    sandbox="allow-same-origin allow-scripts"
    width="700"
    height="600"
    scrolling="no"
    seamless="seamless"
    frameborder="0">
</iframe>

## Data at a Glance

A late season subtropical airmass brought widespread rainfall to the Colorado Front Range September 9-15, 2013, producing widespread flooding from the Pikes Peak Region northward to the Wyoming border. Record amounts of rain fell along the Front Range of Colorado. Hardest hit were Larimer, Boulder and southwest Weld Counties as well as parts of El Paso County and metropolitan Denver. Historic rains and flooding affected 6 major rivers and tributaries, 14 counties, and over a dozen cities and towns in Colorado. Boulder recorded a storm total of 17.15 inches, shattering several records: the daily record, 9.08", the monthly record, 17.24", and the annual record, 30.20". Ft. Carson set a new state record for both 24 hour, 12.46”, and calendar day, 11.85”, rainfall.
Flooding from headwater streams and tributaries moved into the South Platte River near Greeley with widespread flooding and record flood stages as the water made its way downstream into Nebraska. The South Platte at Fort Morgan, CO, peaked near 50,000 cfs (cubic feet per second).
Flood damage encompassed nearly 2,000 square miles of the Colorado Front Range in 18 counties. There were 8 flood fatalities. More than 3,000 people had to be rescued and more than 11,000 evacuated. The storm destroyed 1,500 houses, 200 commercial buildings and 30 state highway bridges. Flood waters damaged nearly 19,000 houses and 800 commercial buildings, 200 miles of roadway, and 20 state highway bridges. Large sections of the counties' roads and highways were washed away, with property and crops completely inundated. Miles of freight and passenger rail lines were washed out. In Weld County, approximately 1,900 gas wells were damaged and had to be closed off as the floodwaters inundated entire communities. Total estimates for damage range from $1 to $2 billion dollars.

<iframe src="/assets/flood-analysis/US-34-damage.jpg"
    sandbox="allow-same-origin allow-scripts"
    width="700"
    height="600"
    scrolling="no"
    seamless="seamless"
    frameborder="0">
</iframe>

Not only was the devastation staggering, but it marked only the second time in Colorado weather history that such a flood happened in September.

The National Weather Service ranked the 2013 flood its top weather story of the 2010-19 decade.

"The surprise of the 2013 flood was that it happened that time of year,'' said state climatologist Russ Schumacher, noting the only other time such a rain event previously happened in September was in 1938. "Events like this that come to mind tend to come in late July and early August during monsoon storms or in May and June with intense thunderstorms.''

## Data Analysis

To begin, I aquired data from USGS for my chosen gauge location and looked at daily stream discharge for the entire period there was data available, from 1979 to 2023.

<iframe src="/assets/temperature-over-time/flood-output-allmeandata.html"
    sandbox="allow-same-origin allow-scripts"
    width="700"
    height="600"
    scrolling="no"
    seamless="seamless"
    frameborder="0">
</iframe>

<iframe src="/assets/temperature-over-time/flood-output-floodonly.html"
    sandbox="allow-same-origin allow-scripts"
    width="700"
    height="600"
    scrolling="no"
    seamless="seamless"
    frameborder="0">
</iframe>

<iframe src="/assets/temperature-over-time/flood-output-allpeakdata.html"
    sandbox="allow-same-origin allow-scripts"
    width="700"
    height="600"
    scrolling="no"
    seamless="seamless"
    frameborder="0">
</iframe>

<iframe src="/assets/temperature-over-time/flood-output-annual_maxima.html"
    sandbox="allow-same-origin allow-scripts"
    width="700"
    height="600"
    scrolling="no"
    seamless="seamless"
    frameborder="0">
</iframe>

<iframe src="/assets/temperature-over-time/flood-output-probability.html"
    sandbox="allow-same-origin allow-scripts"
    width="700"
    height="600"
    scrolling="no"
    seamless="seamless"
    frameborder="0">
</iframe>

<iframe src="/assets/temperature-over-time/flood-output-return-years.html"
    sandbox="allow-same-origin allow-scripts"
    width="700"
    height="600"
    scrolling="no"
    seamless="seamless"
    frameborder="0">
</iframe>






# Results
As we are only getting a monthly view with this dataset, we see that for most summer months, there was at least one day over 85 degrees. We also see that the average temperature for each month tells a different story. We now know that on average for each month, it was never even over 80 degrees. I believe my hypothesis to be correct, that my mother chose a temperature that it would hit every so often, but also would not happen as frequently.
