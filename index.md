---
title       : Quick Check on Storm Damage
subtitle    : Storm Hits and Hurts (1950 - 2011)
author      : Randy Qin
job         : SkywalkerDS
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---

## What to expect when storm hit?

1. Damage to human health (injuries, deaths)
2. Damage to property (millions of dollars)
3. Historical data is good for planning (save lives and save money!)

--- .class #id 

## Under the Hood

The original data is from NOAA, has ~1 million rows, with weather events and damages from 1950 to 2011.  We aggregated the data for each events (985 of them) for plots.


```r
stormDMG <- read.csv("storm-damage.csv")
stormDMG[656:663,]
```

```
##       X           EVTYPE HDMG      PDMG
## 656 656      STORM SURGE   51 763.53604
## 657 657 STORM SURGE/TIDE   16 641.18800
## 658 658  STREAM FLOODING    0   0.00000
## 659 659     STREET FLOOD    0   0.00000
## 660 660  STREET FLOODING    0   0.00000
## 661 661      STRONG WIND  383 175.24145
## 662 662 STRONG WIND GUST    0   0.00000
## 663 663     STRONG WINDS   28   2.31479
```

--- .class #id 

## Super Simple User Interface, Just imagine...

+ Select a few top damaging weather events or segment of top events
+ Choose type of damage to human health or property
+ Result is sorted and plotted with the worst at the top


--- .class #id 

## See it in action, Now!

+ Deployed as Shiny App

<http://skywalkerds.shinyapps.io/storm-app/>


+ Source code available on GitHub

<http://github.com/skywalkerDS/shiny-apps>

