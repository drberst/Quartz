---
title: Chapter 8 Post
created: '2022-03-09T17:12:36.672Z'
modified: '2022-03-09T17:18:27.084Z'
---

# Chapter 8 Post
[[Chapter 8 - Shortcut.lnk|File Explorer Link]]
basic bar, line, and tree map charts. In addition, you saw how to present
measures tied to a geospatial field on a map

Create tables and matrices
Construct bar, column, and pie charts
Build line and scatter charts
Create map-based visualizations

- [x] **Find a dataset that fits well with geo data, time series, or categories for treemap/pie/donut charts**

**2022-03-19 16:12**
The dataset I'm using is pokemon go geo location timestamped data for a few days in July 2016
About 300000 data points
fuck I don't like this
https://www.kaggle.com/datasets/kveykva/sf-bay-area-pokemon-go-spawns
[Pokemon Datasets](https://swhui.github.io/StatisticsinPokemon/datasets/)

**3/21/2022 11am**
[Chapter 8 Forum](https://elearn.nmc.edu/mod/forum/view.php?id=1878058)

For this week I was interested in finding a dataset with latitude and longitude locations, since I'm already pretty comfortable with the basic bar, column, and line charts. 
I've been playing some Pokemon lately, and wondered if there was a dataset I could use related to the game series. 
I found [this site](https://swhui.github.io/StatisticsinPokemon/datasets/) that collects some interested datasets, and decided to go with the [SF Bay Area Pokémon Go Spawns](https://www.kaggle.com/kveykva/sf-bay-area-pokemon-go-spawns). 

The first challenge was that the dates were not in a format Power Bi understood. All the timestamps were using Unix Epoch Time, which is measured as the number of seconds (or milliseconds) since the UNIX epoch (January 1, 1970 00:00:00).
I couldn't find an intuitive way to do this with DAX, but I found a solution online using power query using "#datetimezone(1970,1,1,0,0,0,0,0)"

With the timestamps now in a more readable form, I tried making a few charts, which is when I ran into my second problem. For only a days worth of data for only a small geographic area there was a lot more data than I expected. With 314,105 encounters, each with a lat and lng value, and a timestamp down to the second. There were also 140 unique pokemon in this set, so trying to use any kind of legend or labeling proved difficult. 

The reports I came up with: 
A Matrix to overview and select/filter the data
A treemap to show categories (the pokemon names) and their count

A Map of the geolocation (lat/lng) points
With some breakdown of the part of the day for the encounters
