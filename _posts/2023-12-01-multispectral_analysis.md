---
title: Multispectral Analysis of NAIP Data in Seattle
categories:
- General
feature_image: "https://picsum.photos/2560/600?image=872"
---

Visualize and quantify differences in vegetation health by neighborhood in Seattle, WA.

## Data Choice
As I grew up in Colorado, I always expexted nature to look a little brown in hue. The outdoors in CO are beautiful, but anyone who has visited can tell you that for the most part it is brown. Of course, there is greenery, but it took me moving to Seattle to understand just how brown Colorado was.

Seattle's nickname is Emerald City for a reason. I lived there for a few years and I remember looking out the window of first apartment in the 'Westlake' neighborhood and realizing just how green Seattle was. Even in a major city, there was still vast amounts of greenery, that were true greens.

I moved around for awhile, and I wanted to analyze which neighborhoods were the greenest relative to still being in a large city so if I every move back I can know which neighborhood to live and spend my time in.

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

NAIP data access: The data used were downloaded from the USGS Earth explorer website. There was some technical issues with corrupted data so I will updating this notebook with potentially more correct data in the future.


A great example comes from the [USGS NAS FaST - Flood and Storm Tracker Website]([https://nas.er.usgs.gov/hucs.aspx]). It shows each scaled of the different classification levels.
<p align="center">
  <img width="600" height="400" src="/assets/multispectral/multispectral-imagery.jpg">
</p>

Data Citation: National Agriculture Imagery Program - NAIP Hub Site. (n.d.). https://naip-usdaonline.hub.arcgis.com/ U.S.G.S. (n.d.). The National Agriculture Imagery Program (NAIP) Dataset. EarthExplorer. https://earthexplorer.usgs.gov/

### Spatial Wildfire Occurrence Data for the United States

Data on CONUS fire occurrence between 1992 and 2020 was used from the [the United States Forest Service website](https://www.fs.usda.gov/rds/archive/Catalog/RDS-2013-0009.6)

This data release presents a spatial database documenting U.S. wildfires from 1992 to 2020, supporting the Fire Program Analysis system. The dataset includes 2.3 million geo-referenced wildfire records, covering 180 million burned acres, and conforms to NWCG standards, with redundant records removed. It facilitates linking final fire reports with large fire perimeters and operational situation reports.

## Data Analysis

To begin, I looked at the interaction between the watershed boundaries and the State of Colorado at the HUC-2 level. 

<iframe src="/assets/wildfire/hu2_watersheds.html"
    sandbox="allow-same-origin allow-scripts"
    width="710"
    height="700"
    scrolling="no"
    seamless="seamless"
    frameborder="0">
</iframe>

The HUC-2 level covers an area that is much larger than Colorado, so I began by clipping the watersheds to only be within the borders of CO.

<iframe src="/assets/wildfire/hu2_watersheds_colorado.html"
    sandbox="allow-same-origin allow-scripts"
    width="710"
    height="710"
    scrolling="no"
    seamless="seamless"
    frameborder="0">
</iframe>

At the HU2-level, the watershed boundaries may not give enough detail as to what is actually happening in each part of the state, so I also wanted to analyze the HUC-4 level watersheds. As we can see below, there are far more regions that can help us to better classify the fires that occur in each of these regions.

<iframe src="/assets/wildfire/hu4_watersheds_colorado.html"
    sandbox="allow-same-origin allow-scripts"
    width="710"
    height="710"
    scrolling="no"
    seamless="seamless"
    frameborder="0">
</iframe>

Then, I wanted to look at the total number of fires that occured in each area each year, as well as where the largest fire occured each year. I created some tire series line plots to look at this data, first for the HUC-2:

<iframe src="/assets/wildfire/hu2_lineplotbyregion.html"
    sandbox="allow-same-origin allow-scripts"
    width="1010"
    height="750"
    scrolling="no"
    seamless="seamless"
    frameborder="0">
</iframe>

Followed by same using the HUC-4 data:
<iframe src="/assets/wildfire/hu4_lineplotbyregion.html"
    sandbox="allow-same-origin allow-scripts"
    width="1010"
    height="750"
    scrolling="no"
    seamless="seamless"
    frameborder="0">
</iframe>

To better visualize all of the regions data at once, I also created a combined region line plot for HUC-2 and HUC-4. If you would also like to see specific regions combined, or singled out, click on their names to toggle thhe data for those regions on/off.

<iframe src="/assets/wildfire/hu2_lineplotbyregion_combined.html"
    sandbox="allow-same-origin allow-scripts"
    width="810"
    height="700"
    scrolling="no"
    seamless="seamless"
    frameborder="0">
</iframe>

<iframe src="/assets/wildfire/hu4_lineplotbyregion_combined.html"
    sandbox="allow-same-origin allow-scripts"
    width="810"
    height="700"
    scrolling="no"
    seamless="seamless"
    frameborder="0">
</iframe>

Finally, I also wanted to look at fire density of each region. The units are in terms are hectacres, as they are primarily used as a measurement of land.

First for HUC-2, and then for HUC-4

<iframe src="/assets/wildfire/hu2_density.html"
    sandbox="allow-same-origin allow-scripts"
    width="1050"
    height="710"
    scrolling="no"
    seamless="seamless"
    frameborder="0">
</iframe>

<iframe src="/assets/wildfire/hu4_density.html"
    sandbox="allow-same-origin allow-scripts"
    width="1050"
    height="710"
    scrolling="no"
    seamless="seamless"
    frameborder="0">
</iframe>

# Results
Comparing the data, we see large differences between HUC-2 and HUC-4, which we surprised in our hypothesis. It leads us to continue thinking about the issues of aliasing. With the HUC-2 data, the fire density for the entire western-half is higher than anywhere else, but as we move down in region size to HUC-4, we see that one or two regions are carrying the bulk of that weights. Where-as, if we moved down in scale too much, it would not be tell us enough large-scale information about each region.

For the second part of our hypothessis, we do find that the graphic from USGS detailing the spatial and temporal increase in wildfires is indeed true.

# Data Citations
Short, Karen C. 2022. Spatial wildfire occurrence data for the United States, 1992-2020 [FPA_FOD_20221014]. 6th Edition. Fort Collins, CO: Forest Service Research Data Archive. https://doi.org/10.2737/RDS-2013-0009.6

Watershed Boundary Dataset (WBD). U.S. Geological Survey / USDA Natural Resources Conservation Service / U.S. Environmental Protection Agency. https://data.nal.usda.gov/dataset/watershed-boundary-dataset-wbd. Accessed 2023-10-11.
