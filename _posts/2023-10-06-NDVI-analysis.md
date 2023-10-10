---
title: NDVI Analysis and Working with Raster Data
categories:
- General
feature_image: "https://picsum.photos/2560/600?image=872"
---

Using NDVI raster data to analyze vegetation regrowth after the Royal Gorge Fire that occurred in 2013 just outside of Cañon City, CO.

## Data Choice
A popular attraction in the mountains of CO, west of Pueblo, is the Royal Gorge Canyon Train and Suspension Bridge. My family had a trip planned to go back for the first time in a decade. The week before we went, a fire sparked and the park shut down, for 9 months. Even after that, everyone who went told us that it was sad to see the once lively park covered in burn marks. It has now been another decade since the fire and when choosing a dataset to analyze, I was curious to see how long it took for the landscape to recover. Below I analyze NDVI data to assess vegetation regrowth in the area where the fire occurred. Watch the following video to see how the Royal Gorge park fared after 10 years.

<div class="scripps_iframe_embed" style="position:relative"><div style="display:block;width:100%;height:auto;padding-bottom:56.25%;"></div><iframe id="da-iframe" allowfullscale="" style="position:absolute;top:0;left:0;width:100%;height:100%;" border="0" height="100%" frameborder="0" webkitallowfullscreen="" allowfullscreen="" mozallowfullscreen="" scrolling="no" src="https://assets.scrippsdigital.com/cms/video/player.html?video=https://content.uplynk.com/fa36cd464670483cb1859781a179cf62.m3u8&mp4=https://x-default-stgec.uplynk.com/ausw/slices/fa3/b2da66f716dc47439b09dfbbeb8a98d1/fa36cd464670483cb1859781a179cf62/fa36cd464670483cb1859781a179cf62_e.mp4&autoplay=false&purl=/news/ashes-to-renewal/royal-gorge-rebuild-ten-years-later&ads.iu=/6088/ssp.koaa/news/ashes-to-renewal/royal-gorge-rebuild-ten-years-later&ads.proxy=1&poster=https://x-default-stgec.uplynk.com/ausw/slices/fa3/b2da66f716dc47439b09dfbbeb8a98d1/fa36cd464670483cb1859781a179cf62/poster_a2824f9e042e480c954fb19aefa8bacb.jpg&title=Rebuilding%20the%20Royal%20Gorge%2C%20ten%20years%20after%20the%20flames%20settled&kw=%272013%20FIRES%20%2C10%20YEARS%20%2C14000%20ACRES%20%2C2013%20%2C2013%20FIRE%20%2C488%20HOMES%20%2C500%20HOMES%20%2CACRES%20%2CAMERICAN%20NATURAL%20HISTORY%20%2CAMERICAS%20BRIDGE%20&contplay=*recent&mute=0&tags=Ashes%20to%20Renewal%2CHomepage%20Showcase%2CNews5%20Originals&section=Ashes%20to%20Renewal&cust_params=temp%3D%26weather%3D&host=koaa.com&s=koaa&ex=1" allow="autoplay; fullscreen"></iframe></div>

## Data at a Glance

Royal Gorge Fire Quick Facts

 * First reported at 1pm June 11th, 2013.
 * 3,218 acres burned.
 * 32 out of 1,292 wooden planks burned on the Royal Gorge Bridge.
 * 48 out of 52 buildings in the Royal Gorge Bridge and Park were lost.
 * The Royal Gorge Bridge and Park was closed for 9 months. 
 * The Royal Gorge Fire was fully contained on June 16th, 2013.
 * No injuries were reported, and no residential homes were lost.
 * Cost to rebuild park: $30 million
 * About 25,000 pounds of native grass and wildflower seeds were planted.

The image below that was taken in 2013 and outlines the fire boundary in white dots with a red circle where the suspension bridge occurs from [Wikipedia]([(https://en.wikipedia.org/wiki/File:ISS_image_of_Royal_Gorge,_Canon_City,_Colorado,_USA,_wildfire_burn_scars_with_markings,_rotated_-30_degrees_and_cropped,_2013.jpg)]) 

<p align="center">
  <img width="700" height="600" src="/assets/ndvi/royal-gorge-location.jpg">
</p>



## Why NDVI for Vegetation Analysis
Normalized Difference Vegetation Index (NDVI) quantifies vegetation by measuring the difference between near-infrared (which vegetation strongly reflects) and red light (which vegetation absorbs). Healthy vegetation (chlorophyll) reflects more near-infrared (NIR) and green light compared to other wavelengths. But it absorbs more red and blue light.

This is why our eyes see vegetation as the color green. If you could see near-infrared, then it would be strong for vegetation too.

## Data Analysis

To begin, I acquired the raster data from [Wildland Fire Interagency Geospatial Services (WFIGS) Historic Perimeters 2013 API explorer site](https://data-nifc.opendata.arcgis.com/datasets/nifc::historic-perimeters-2018/api) and downloaded it using the [APPEEARS](https://appeears.earthdatacloud.nasa.gov/) API (Application Programming Interface) for the royal gorge location and looked at the NDVI.

First, I looked at the NDVI difference for the immediate pre-fire and post-fire years, 2012 to 2014. 

<iframe src="/assets/ndvi/ndvi_pre_post_fire_years_2012_2014.html"
    sandbox="allow-same-origin allow-scripts"
    width="710"
    height="500"
    scrolling="no"
    seamless="seamless"
    frameborder="0">
</iframe>

We can see some areas with very clear differences in the NDVI spatially, in order to get a better idea as to where the edges of the fire were, I next plotted the boundary of the fire on top of the NDVI plot. Then I expanded the data to be from 2010 to 2023, so we can get a better picture of the full effects of the fire.


<iframe src="/assets/ndvi/ndvi_pre_post_fire_years_2010-2023.html"
    sandbox="allow-same-origin allow-scripts"
    width="710"
    height="500"
    scrolling="no"
    seamless="seamless"
    frameborder="0">
</iframe>

To get a better understanding of the values we are seeing, I also then created a histogram to see the spread of values, for the same parameters as the above plot.

<iframe src="/assets/ndvi/ndvi_pre_post_fire_years_2010_2023_histogram.html"
    sandbox="allow-same-origin allow-scripts"
    width="710"
    height="300"
    scrolling="no"
    seamless="seamless"
    frameborder="0">
</iframe>

Finally, to see how the area has fared over the last decade, I plotted values from before and after the fire, while taking a more in depth look at if the fire dropped more inside the boundary than outside. This plot shows the values as well for 2010 - 2023 and shows a vertical line where the fire occurred. Despite 25,000 pounds of planting wildflowers and grasses being planted in the area, the area has barely seen any vegetation recovery.

<iframe src="/assets/ndvi/ndvi_line-plot.html"
    sandbox="allow-same-origin allow-scripts"
    width="710"
    height="300"
    scrolling="no"
    seamless="seamless"
    frameborder="0">
</iframe>


# Results
It will take decades for the trees and vegetation to ever recover following the royal gorge fire. A research team from Australian National University found that forests’ ability to recover from a fire can stretching to more than 80 years. This means that we may continue to see devastated landscapes post-fire for many years to come, impacting the ability for wildlife to reemerge and humans to recreate in these areas. 

A University of Colorado Boulder study noted that in the Southern Rocky Mountains the post-fire landscape is becoming unsuitable for future growth of ponderosa pine and Douglas fir. This finding from their research reveals that if fires continue to drastically harm the soil quality and ecosystem health, it may be hard for local trees to regrow in those areas.

Someday I hope to revisit the area, and hopefully in my lifetime it will look just like it did when I was a kid.

# Data Citations

Didan, K. (2021). MODIS/Aqua Vegetation Indices 16-Day L3 Global 250m SIN Grid V061. NASA EOSDIS Land Processes Distributed Active Archive Center. Accessed 2023-10-06 from https://doi.org/10.5067/MODIS/MYD13Q1.061. Accessed October 6, 2023. 
