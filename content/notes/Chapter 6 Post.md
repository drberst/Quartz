---
attachments: [forum6-2.png, forum6-3.png, forum6.png]
title: Chapter 6 Post
created: '2022-03-07T16:28:21.519Z'
modified: '2022-03-08T14:15:20.429Z'
---

# Chapter 6 Post

For this I found a [data set of TED talks](https://www.kaggle.com/ashishjangra27/ted-talks) that was scrapped from their website. Like in the lab, I wanted to calculate a few sums and ratios and put them in a matrix with filters.

I wish the data set I found had categories or topics, but I was able to break things down by month and year which still proved interesting.

I started with a CSV file that included: title, author, date (month / year), views, likes, and a url to the talk itself. I added columns for month, month number, and year, based off the date column.

From there I created several measures using Sum, Calculate, Divide, and variables.

The main issue I had at first was getting the totals using the ALL() function. But I was able to get it working.
![Image reference][1]
Next, I thought I had a problem in my "Views to Likes" ratios because they were all basically 3%. But I did some checking, calculated some values manually, and it seems like just coincidentally the likes a TED talk gets is almost always about 3%. The smallest ratio was for the single video from 1994 (2.86%). The largest was for 1973 (3.15%) which also had only a single video. If I ignore years with less than 100 videos the ratios narrow, with a range of only 3.02% (2007) to 3.06% (2017).

I also looked at the view count by month, and February, June, and November stood out to me as notably higher. I thought it might have to do with the fact that the TED conference is primarily an anual event, so I looked into the date history at https://www.ted.com/about/conferences/past-teds, and it turns out a significant portion of talks happened in February/March, which I think explains the spike in views for those months.

![Image]
### paths
[1]: ./forum6.png

### Attachments
![bane](@attachment/Clipboard_2022-03-07-11-33-58.png)

