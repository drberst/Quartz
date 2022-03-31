---
attachments: [Clipboard_2022-03-07-14-20-59.png, Clipboard_2022-03-07-14-23-19.png, Clipboard_2022-03-07-14-25-35.png, Clipboard_2022-03-07-14-26-17.png, Clipboard_2022-03-07-14-28-10.png, Clipboard_2022-03-07-14-28-19.png]
title: Chapter 7 Post
created: '2022-03-07T17:10:02.011Z'
modified: '2022-03-07T19:31:04.826Z'
---

# Chapter 7 Post

Steam dataset: https://www.kaggle.com/luthfim/steam-reviews-dataset
Month to date
Year to Date

First I imported csv
Then made date table and linked
![](@attachment/Clipboard_2022-03-07-14-20-59.png)
Then tried Measures: 
  Get count of good reviews and bad
    Tried to use IF(steam_reviews[recommendation] = "Recommended",1,0) and then summing that column
    but a found a better way using CALCULATE ( COUNTROWS ( steam_reviews ), steam_reviews[recommendation] = "Recommended" )
  Bad reviews was basically the same
  Total reviews just adds the Good and Bad measures together
![](@attachment/Clipboard_2022-03-07-14-23-19.png)
  Then added a few from the chapter, like ytd good reviews, month to month growth, and year to year growth 
![](@attachment/Clipboard_2022-03-07-14-25-35.png)

The main interesting things I found about this data
* Reviews were heavily dominated by a select few games (less than 5), usually online multiplayer games (Rocket League, PubG, Rust, GTA5)
(the top 5 games had roughly 50x as many reviews as the next 5 down)
![](@attachment/Clipboard_2022-03-07-14-28-19.png)

