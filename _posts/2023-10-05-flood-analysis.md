---
title: Flood Event and Water Year Analysis
categories:
- General
feature_image: "https://picsum.photos/2560/600?image=872"
---

The Front Range Flood Event was a significant flood in Northern Colorado that occured in September, 2013.

## Data Choice
My first experience fully understanding the effects of floods, was when this event occured. We took a field trip to Loveland, CO to look at the damage. A park I used to go to when I was young was under 10 feet of debris. I wanted to analyze this flood, and see how likely it is to happen again, and if the water year had low probability to occur again. I found a gage location near that park to analyze the stream discharge data in order to understand the return year and probability.

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

To begin, I aquired data from [USGS]([https://waterdata.usgs.gov/nwis/dv?cb_00060=on&format=rdb&site_no=06741510&legacy=&referred_module=sw&period=&begin_date=1979-01-01&end_date=2023-10-02]) for my chosen gauge location and looked at mean daily stream discharge for the entire period there was data available, from 1979 to 2023.

<iframe src="/assets/flood-analysis/flood-output-allmeandata.html"
    sandbox="allow-same-origin allow-scripts"
    width="700"
    height="600"
    scrolling="no"
    seamless="seamless"
    frameborder="0">
</iframe>

Here is a closer look at the exact time range of the flood that occured in September, 2013 at the same gauge location. Note how many days it took for the stream to recover as well.

<iframe src="/assets/flood-analysis/flood-output-floodonly.html"
    sandbox="allow-same-origin allow-scripts"
    width="700"
    height="600"
    scrolling="no"
    seamless="seamless"
    frameborder="0">
</iframe>

As the stream discharge values above are a mean, I also downloaded the annual instantaneous peak discharge values from [USGS](https://waterdata.usgs.gov/nwis/dv?cb_00060=on&format=rdb&site_no=06741510&legacy=&referred_module=sw&period=&begin_date=1979-01-01&end_date=2023-10-02). Here is a look for the same time range using the instantaneous values.
<iframe src="/assets/flood-analysis/flood-output-allpeakdata.html"
    sandbox="allow-same-origin allow-scripts"
    width="700"
    height="600"
    scrolling="no"
    seamless="seamless"
    frameborder="0">
</iframe>

In order to compare the difference between the mean daily and the annual peak instantaneous values, I annualized the daily data, and you can compare the difference below. Note how much smaller the values are from the mean vs. the peak.

<iframe src="/assets/flood-analysis/flood-output-annual_maxima.html"
    sandbox="allow-same-origin allow-scripts"
    width="700"
    height="600"
    scrolling="no"
    seamless="seamless"
    frameborder="0">
</iframe>

As we analysis the likelihood of this flood happening again, clearly using the mean and instantaneous values will make a large difference. Going forward I will do calculations using both values to compare.

Instantaneous events are in purple, with the annually sampled mean in black, with a log scale along the y-axis for probability. We can see that the probability for the 2013 events are in star markers, and you can hover over them to see their exact values. Because of the mean usage, some years overall are much less likely to occur than the 2013 event as a hwole. So we see that the instantaneous values, show that the 2013 event was the least probable for all years in this location since 1979.

<iframe src="/assets/flood-analysis/flood-output-probability.html"
    sandbox="allow-same-origin allow-scripts"
    width="700"
    height="600"
    scrolling="no"
    seamless="seamless"
    frameborder="0">
</iframe>

Finally, I also calculated the return period for the 2013 flood. We see a similar trend where the 2013 flood event itself has the highest return period. But 2013 as a whole was lower than other years when summed annually.
<iframe src="/assets/flood-analysis/flood-output-return-years.html"
    sandbox="allow-same-origin allow-scripts"
    width="700"
    height="600"
    scrolling="no"
    seamless="seamless"
    frameborder="0">
</iframe>

# Results
When studying exact short-time frame events, using the instantaneous values gives us clues for that event. But in order to evaluate the trend for the full water year, using the mean values gives us that information.

Overall, I learned that the 2013 water year was not the overall worst year, but the event itself was the rarest event seen in this area since at least 1979.
