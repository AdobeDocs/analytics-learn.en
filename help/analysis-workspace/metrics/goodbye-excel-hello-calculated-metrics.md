---
title: Goodbye Excel, hello calculated metrics
description: Learn the benefits of using calculated metrics in Adobe Analytics and how they can provide you with a continuous, dynamic view of your data in this article.
feature: Calculated Metrics
role: User
level: Experienced
doc-type: Article
last-substantial-update: 2023-05-02
jira: KT-13178
thumbnail: KT-13178.jpeg
exl-id: 1ced644c-db66-4084-a5da-10b028f7e8ac
---
# Goodbye Excel, hello calculated metrics

Learn the benefits of using calculated metrics in Adobe Analytics and how they can provide you with a continuous, dynamic view of your data in this article.

Hey! Why are you in Excel right now? I mean, I know why. You've got reporting to get to the right people. You're busy entering data from Adobe Analytics and calculating conversion rates, charting them, and preparing to put them all into a PowerPoint that's heading off to decision-makers. I really hope you're at least using Report Builder to do it, but I know that some of you are manually copying and pasting data from a Workspace to Excel.
 
Why?
 
Why go through a manual process every month? Why present a static view once a month instead of a continuous, dynamic view? Why copy that into PowerPoint? Why not create Calculated Metrics in Adobe Analytics directly?
 
## Calculated Metrics are Powerful
 
Calculated Metrics are powerful, but even the basic mathematical functions are really useful and serious improvement over doing the math in Excel. Let's look at some of the benefits and some use cases:
 
1. **Calculated Metrics are Current and Dynamic**
 
    When you export numbers from Adobe Analytics, they're locked in a point in time. You absolutely need to know how your site or app performed the month before, but how do decision makers keep track of how things are going mid-month? If your conversion rate plunges for one day and then reverts to the mean by the end of the month, will you know? That plunge could be valuable data that reveals an important telemetry issue, or even more vital, a change in visitor behavior. With a calculated metric, you can chart this and see it the day it happens, leaving you ready to respond. 
 
1. **Calculated Metrics Save You Time**
 
    I've been there. Copy/paste. Enter the formula or drag the cell above it down. Click on the chart and change the range so you've got the last twelve or thirteen months. Now copy the chart. Now do it again. And again. And again. Send out the PowerPoint. It's tedious and time consuming and it feels like you have to do it every month forever. 
 
    Instead you can create a Workspace that uses your calculated metric, have Last Twelve or Thirteen Full Months as your date range, and have the data and the chart update automatically at the stroke of midnight on the first day of every month. The recipients can have direct access to the Workspace. They can have a PDF copy automatically emailed to them on the first day of the month or after you use Text Visualizations to add your commentary on the data (you know, the fun part of reporting). 
 
1. **Calculated Metrics Can Be Applied to Big Sets of Data**
 
    You could export all of the product names into Excel and begin calculating conversion rates and revenue per visitor, but this becomes a hassle when you have 100,000 or so. Not an issue with Calculated Metrics. Drop your dimension into a table as usual and then use your Calculated Metrics as the metrics. Now you've got a dynamic sortable table that will update automatically as products or whatever dimension you're using are added to your catalogue.  
 
1. **Calculated Metrics Prevent Mistakes**
 
    Excel errors happen. We've all been there. Heck, the entire economy of Greece and the reputation of two esteemed academics were ruined because of an Excel formula error. You probably don't have a European economy riding on your Excel skills, but there's definitely some decision about budgets that's going to shift based on your numbers. Using Calculated Metrics means you can build a metric, have it QA'd, and then not worry about it again.  

### Now that we've gone over the benefits of using calculated metrics, let's look at how we can put them into practice 
 
**Use Case 1 : Conversion Rates**
 
Most conversion rates are just simple division. Divide the number of conversions by the number of visitors or visits. Divide the number of page views for the final page of a funnel by the number of pages view for the first page of a funnel. Divide the number of internal campaign clickthroughs by the number of impressions. All of these can easily be done as calculated metrics and placed in a dashboard enjoying low data latency, updating visualizations, and greater shareability. 
 
**Use Case 2: Internal Search**
 
Internal search is one of the most important tools for understanding your site. Site search results tell you what your visitors are interested in and whether they can easily find it through navigation or not. You have to be able to tell whether your site search is working well and using a bit of basic addition and division can give you that answer. 
 
Let's start with search results. You want to know if a search term gets results or brings up nothing. Those are usually separate events. Do you want to go through the trouble of getting a third event for all internal site searches added? Instead, give your devs a break and use Calculated Metrics to add Internal Search: Results and Internal Search: No Results together to get Total Internal Searches. 
 
What percentage of searches return no results? Divide Internal Search: No Results by that new Total Internal Searches Calculated Metric. Now you know if creating new content to match those search terms is urgent, or if maybe your content team can tackle higher priorities.  
 
We want to know how many of those searches with results get clickthroughs and usually have a separate metric for that as well. Use Calculated Metrics to divide the number of clickthroughs by the number of times that term brought up search results and display it as a percentage. Now you have the clickthrough rate for every internal search term on your site. You can isolate the search terms that are bringing up unhelpful results. It's got all historical data available to you so you can chart it, and as you make improvements, you can easily see if they're working by watching that rate go up or down. 
 
Divide the number of internal searches by the number of searching visitors. You have searches per visitor for each term. If that number is high (the closer it is to 1.0 the better) you have one of two possible problems. Either the results being clicked on are bad and your visitors are doing multiple searches to find the best results, or they can't find the pages they're looking for through nav. 
 
How can you measure if those key pages are findable through your nav? Create a calculated metric for page views that followed a search results page view. Divide that by total page views for that page. Now you know the percentage of page views that came from search results. If you have a high percentage, you probably have some work to do on navigation. 
 
### Calculated Metrics Are Powerful 
 
I hope this has shown you some of the possibilities of using basic mathematical functions in Calculated Metrics and that you'll start building some yourself. This only begins to describe the possibilities of the math you can do in Calculated Metrics, even with four simple functions. Calculated Metrics can help you understand visitor behavior on an entirely new level and once you've got the hang of it, you've opened the door to using more complex functions that are also available to you.

## Author

This document was written by:

![Gittai headshot](assets/gittai.png)

**Gitai Ben-Ammi**, Principal Consultant at Concentrix Catalyst

Adobe Analytics Champion
