---
title: "Hello R Markdown"
author: "Frida Gomam"
date: 2015-07-23T21:13:14-05:00
categories: ["R"]
tags: ["R Markdown", "plot", "regression"]
---

```{r setup, include=FALSE}
knitr::opts_chunk$set(collapse = TRUE)
```

# R Markdown


```{r,echo=F}
require(leaflet)
latlon <- c(33.79667, -84.32346) # emory
ecc_label <- "Room 2052, Wayne Rollins Building"
ecc_popup <- "Take the elevator to the second floor, \nthen exit left and take the first left."
map <- leaflet() # initiate the leaflet map object
map <- addTiles(map) # add the actual map tiles to the leaflet object
map <- addMarkers(map,latlon[2],latlon[1],label=ecc_label,popup=ecc_popup) 
map 
```