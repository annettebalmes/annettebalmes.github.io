---
title: Multispectral Analysis of NAIP Data in Seattle
categories:
- General
feature_image: "https://picsum.photos/2560/600?image=872"
---

Visualize and quantify differences in vegetation health by neighborhood in Seattle, WA.

## Data Choice
As I grew up in Colorado, I always expexted nature to look a little brown in hue. The outdoors in CO are beautiful, but anyone who has visited can tell you that for the most part it is brown. Of course, there is greenery, but it took me moving to Seattle in 2019 to understand just how brown Colorado was.

Seattle's nickname is Emerald City for a reason. I lived there for a few years and I remember looking out the window of first apartment in the 'Westlake' neighborhood and realizing just how green Seattle was. Even in a major city, there was still vast amounts of greenery, that were true greens.

I moved around for awhile, and I wanted to analyze which neighborhoods were the greenest relative to still being in a large city so if I every move back I can know which neighborhood to live and spend my time in. I downloaded the neighborhood data from the Seattle Public Utilities website.

<iframe src="/assets/multispectral/seattle-neighborhoods.html"
    sandbox="allow-same-origin allow-scripts"
    width="500"
    scrolling="no"
    seamless="seamless"
    frameborder="0">
</iframe>

The above interactive plot details each neighborhoods in Seattle, and their sub-neighborhoods. For example, I lived in Westlake, which is apart of the Cascade Neighborhood. 

## Data at a Glance

### NAIP Multispectral Data

The National Agriculture Imagery Program (NAIP) provides multispectral aerial imagery data for agricultural and land use applications. NAIP typically captures data in multiple spectral bands, including Red, Green, Blue, and Near-Infrared. Some NAIP datasets may have additional bands, such as panchromatic or thermal infrared, depending on the year and location according to the NAIP.

Since I moved to Seattle in 2019, I wanted to look at NAIP from 2019-present to see what would have been the best neighborhood to live in in the time I lived there, or if I moved back today.

NAIP data access: The data used were downloaded from the USGS Earth explorer website. There was some technical issues with corrupted data so I will updating this notebook with potentially more correct data in the future.

<p align="center">
  <img width="600" height="400" src="/assets/multispectral/multispectral-imagery.jpg">
</p>

### Spatial Wildfire Occurrence Data for the United States

Data on CONUS fire occurrence between 1992 and 2020 was used from the [the United States Forest Service website](https://www.fs.usda.gov/rds/archive/Catalog/RDS-2013-0009.6)

This data release presents a spatial database documenting U.S. wildfires from 1992 to 2020, supporting the Fire Program Analysis system. The dataset includes 2.3 million geo-referenced wildfire records, covering 180 million burned acres, and conforms to NWCG standards, with redundant records removed. It facilitates linking final fire reports with large fire perimeters and operational situation reports.

## Data Analysis

Below are chlorpleth plots of the statistics for each neighborhood.

Maximum:
<iframe src="/assets/mulispectral/chloropleth-seattle-2019-present-max.html"
    sandbox="allow-same-origin allow-scripts"
    width="500"
    height="500"
    scrolling="no"
    seamless="seamless"
    frameborder="0">
</iframe>

Describe Maximum

Minimum:
<iframe src="/assets/mulispectral/chloropleth-seattle-2019-present-minimum.html"
    sandbox="allow-same-origin allow-scripts"
    width="500"
    height="500"
    scrolling="no"
    seamless="seamless"
    frameborder="0">
</iframe>

Describe Min

Mean:
<iframe src="/assets/mulispectral/chloropleth-seattle-2019-present-mean.html"
    sandbox="allow-same-origin allow-scripts"
    width="500"
    height="500"
    scrolling="no"
    seamless="seamless"
    frameborder="0">
</iframe>

Describe Mean

25th Percentile:
<iframe src="/assets/mulispectral/chloropleth-seattle-2019-present-q25.html"
    sandbox="allow-same-origin allow-scripts"
    width="500"
    height="500"
    scrolling="no"
    seamless="seamless"
    frameborder="0">
</iframe>

Describe q25

75th Percentile:
<iframe src="/assets/mulispectral/chloropleth-seattle-2019-present-q75.html"
    sandbox="allow-same-origin allow-scripts"
    width="500"
    height="500"
    scrolling="no"
    seamless="seamless"
    frameborder="0">
</iframe>

Describe q75

Standard Deviation:
<iframe src="/assets/mulispectral/chloropleth-seattle-2019-present-sd.html"
    sandbox="allow-same-origin allow-scripts"
    width="500"
    height="500"
    scrolling="no"
    seamless="seamless"
    frameborder="0">
</iframe>

Describe sd

# Results


# Data Citations
National Agriculture Imagery Program - NAIP Hub Site. (n.d.). https://naip-usdaonline.hub.arcgis.com/ U.S.G.S. (n.d.). The National Agriculture Imagery Program (NAIP) Dataset. EarthExplorer. https://earthexplorer.usgs.gov/

Seattle Public Utilities. (2020). Neighborhood Map Atlas Neighborhoods. https://data-seattlecitygis.opendata.arcgis.com/maps/SeattleCityGIS::neighborhood-map-atlas-neighborhoods.
