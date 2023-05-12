---
layout: post
title: Mapping the Danger Zones 
subtitle: A Comprehensive Analysis of England's Trafic Accidents
#author: Jeffrey
categories: Story
banner: 
  video: https://cogniom.com/wp-content/uploads/2019/02/Cars-Driving-on-Highway-Blurred.mp4
  #video: https://vjs.zencdn.net/v/oceans.mp4
  #video: <iframe width="560" height="315" src="https://www.youtube.com/embed/Fgc8iBdiG-I?controls=0" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay=1; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
  #video: <iframe src="https://player.vimeo.com/video/824901997?h=a7b31f3a9d&amp;badge=0&amp;autopause=0&amp;player_id=0&amp;app_id=58479" width="400" height="300" frameborder="0" allow="autoplay; fullscreen; picture-in-picture" allowfullscreen title="videotest"></iframe>
  loop: true
  #volume: 0.8
  start_at: 0.5
  image: "/assets/images/banners/home.jpeg"
  opacity: 0.418
  background: "#000"
  height: "100vh"
  min_height: "38vh"
  heading_style: "font-size: 4.25em; font-weight: bold; text-decoration: underline"
  subheading_style: "color: gold"
#tags: jekyll theme yat
sidebar: []
---

By the end of 2010, England was home to more than 52 million people [<a href="https://www.ons.gov.uk/peoplepopulationandcommunity/populationandmigration/populationestimates/bulletins/annualmidyearpopulationestimates/2013-12-17">1</a>] and almost 30 million vehicles [<a href="https://www.gov.uk/government/statistical-data-sets/vehicle-licensing-statistics-data-tables#all-vehicles">2</a>]. Unfortunately, this makes traffic accidents inevitable. In fact, between 2005 and 2010, on average almost 3.5 people were seriously injured in a traffic accident in England every day! It is therefore highly relevant to explore data concerning traffic accidents nationwide. This data story covers traffic accidents in England from 2005 to 2010.



## Watch out in Birmingham and Manchester! Or?
Do you ever wonder where in England traffic is most dangerous? Let’s look into it. England is divided into 335 local authority districts. The map below shows us the most dangerous districts to get into traffic. Try and zoom in on the areas you think are the most dangerous!

<iframe src="/assets/images/banners/choropleth.html"
    sandbox="allow-same-origin allow-scripts"
    width="1200"
    height="620"
    scrolling="no"
    seamless="seamless"
    frameborder="0">
</iframe>

Figure 1: Choropleth map showing the number of traffic accidents in all 335 local authority districts of England. test


This map makes it clear that we need to look twice before we cross the road in Birmingham and Manchester. But is that the whole story? Did you try to zoom in on the London districts? They really don’t look very dramatic. But considering the fact that the capital city has a population of more than 5 times the populations of Birmingham and Manchester combined [<a href="https://da.wikipedia.org/wiki/Manchester">3</a>], [<a href="https://en.wikipedia.org/wiki/Birmingham">4</a>], [<a href="https://en.wikipedia.org/wiki/London">5</a>], surely we would expect to see a hotspot for traffic accidents here. Let’s have a look at the number of accidents across the 10 most populous cities in England:

<iframe src="/assets/images/banners/Cities.png"
    sandbox="allow-same-origin allow-scripts"
    width="1200"
    height="900"
    scrolling="no"
    seamless="seamless"
    frameborder="0">
    
</iframe>
Figure 2: Bar chart showing the combined number of traffic accidents for the 10 largest cities in England


Wow, London takes first place and far outranks the other cities when it comes to traffic accidents. Maybe the previous map made Londoners feel a tad too safe. So how about instead of dividing England into districts, we simply divide it into square kilometers? Have a look at the following map:

<iframe src="/assets/images/banners/2DHistogram.png"
    sandbox="allow-same-origin allow-scripts"
    width="1200"
    height="620"
    scrolling="no"
    seamless="seamless"
    frameborder="0">
</iframe>
Figure 3: 2D histogram showing the number of traffic accidents per square kilometer


Allright, our expectations are confirmed. Looking twice before crossing the road in Birmingham and Manchester might not be such a bad idea. But definitely look three times if you’re ever in London!


## England’s most dangerous road!

Now, let’s find the most dangerous road in England! Most of the roads in England are categorized into 4 different classes: A, B, C, and M. A-roads are the main roads connecting towns and cities, B- and C-roads are smaller roads connecting small towns and villages and M-roads are high-speed motorways [<a href="https://www.bituchem.com/knowledge-hub/what-are-the-different-types-of-road-in-the-uk/">6</a>]. First, we can get an overview of where most of the accidents occur by looking at the bar chart below:

<iframe src="/assets/images/banners/RoadClasses.png"
    sandbox="allow-same-origin allow-scripts"
    width="1200"
    height="620"
    scrolling="no"
    seamless="seamless"
    frameborder="0">
</iframe>
Figure 4: Overview of the number of accidents for each of the road types


The vast majority of accidents appear to occur on A-roads, so we should take a closer look at those. Luckily, these are some of the most well-known roads in England, so it will be easier to find information on them later. For now, let’s see the top 30 A-roads in England with the most accidents.

<iframe src="/assets/images/banners/Top30Roads.png"
    sandbox="allow-same-origin allow-scripts"
    width="1200"
    height="620"
    scrolling="no"
    seamless="seamless"
    frameborder="0">
</iframe>
Figure 5: Accumulated number of accidents for each of the top 30 roads.


It looks like road A6 is the most dangerous road with over 6000 accidents, closely followed by road A38. A quick Google search reveals that A6 and A38 are 453.8 km and 469.9 km long, respectively [<a href="https://en.wikipedia.org/wiki/A6_road_(England)">7</a>], [<a href="https://en.wikipedia.org/wiki/A38_road">8</a>]]. These are some of the longest roads in England, which might explain why a larger number of accidents occur here. 

Therefore, another way of looking at it would be to calculate how many accidents happen per kilometer of road for each of the top 30 roads.

<iframe src="/assets/images/banners/Top30RoadsNorm.png"
    sandbox="allow-same-origin allow-scripts"
    width="1200"
    height="620"
    scrolling="no"
    seamless="seamless"
    frameborder="0">
</iframe>
Figure 6: Similar to Figure 5, this bar chart shows the number of traffic accidents for each of the top 30 roads, but now it is normalized by the length of each given road.


Looks like we have a clear winner! Road A406 hosts the most accidents per kilometer. And the long roads A6 and A38 are bumped way down the list. So road A406 is the one which Englishmen should fear the most. But is this really the case? Actually, it seems not to be. It turns out that in recent years, the media has focused more on the danger of road A41. It is no coincidence that this road appears on our list of the 30 most dangerous roads holding 19th place. The A41 runs between London and Birkenhead (close to Liverpool) and is approximately 328 km long. In May 2021 it was deemed one of the most dangerous roads for young drivers by The AA Charitable Trust [<a href="https://planetradio.co.uk/greatest-hits/beds-bucks-herts/news/a41-hertfordshire-dangerous-young-drivers/">9</a>]. Additionally, in March 2022 hundreds of residents in Hemel Hempstead signed a petition aimed at improving the safety of road A41 [<a href="https://www.watfordobserver.co.uk/news/19986225.a41-hemel-hempstead-hundreds-sign-petition-calling-safety-measures/">10</a>], and in August 2022 an article from the Shropshire Star reported that 
“the road has been the subject of concern for a number of years, with campaign groups pressing for action to improve the safety record of the route.”[<a href="https://www.shropshirestar.com/news/transport/2022/08/08/time-to-act-over-dangerous-a41-after-shocking-number-of-deaths-and-injuries-is-revealed/">11</a>]. 

So if our 19th-placed road is considered one of the most dangerous roads in England, which other roads do the Englishmen fear? Perhaps the roads considered most dangerous are not even on our top-30 list. And if A41 is especially dangerous for young drivers, maybe we should try and take a look at a more customized data representation. Below is an interactive plot, where you can choose your age, gender, and the roads in your area. The plot shows you which maneuvers cause the most accidents under the specified conditions. Take a look, and play around with the interactive plot!


<iframe src="/assets/images/banners/dashboard2.html"
    sandbox="allow-same-origin allow-scripts"
    width="1200"
    height="620"
    scrolling="no"
    seamless="seamless"
    frameborder="0">
</iframe>
