---
title: A Comprehensive Guide for Transitioning to Adobe Analytics from Google Analytics
description: One of the biggest challenges in transition between any tool is learning where to find equivalent functionality and learning how to use it efficiently. This discussion is part of a larger guide to help users transition to Adobe Analytics easier.
feature: Third-party Integration
role: User
level: Beginner
doc-type: feature video
thumbnail: 34749.jpg
kt: 9830

---

# A Comprehensive Guide for Transitioning to Adobe Analytics from Google Analytics

## 1. Introduction

One of the largest challenges in transitioning between any tool is learning where to find equivalent functionality and learning how to use it efficiently. This discussion is part of a larger guide to help users transition to Adobe Analytics (either as a new user, or one coming from Google Analytics) easier. An in-depth comparison to GA; as the most likely comparative tool that most users will have familiarity with; is provided to help users correlate existing knowledge to the new toolset. While there is no substitute for practice; this will help get you started and hopefully reduce the frustrations you may encounter during this time (or even as a refresher after you start to get into the swing of things).

We should also just have a quick terminology comparison:

| **Description** | **Adobe Analytics** | **Google Analytics** |
|--------------------------------------------------------------------------------------------------------------------------------|---------------------|----------------------|
| An event metric that represents a page (or screen on an app) has been viewed | Page View| Pageview |
| A metric that represents a group of interactions on your website or app that take place in the same time frame | Visit | Session |
| A metric that defines an identified device (based on multiple criteria including cookies and other behavior patterns to stitch user information) | Unique Visitor | User |

## 2. The Interfaces

One of the things I see most often when people compare Adobe Analytics and Google Analytics is that Adobe has a lot going on - it's daunting to people. This is true, but it's also; believe it or not; a strength, not a weakness. Adobe provides a wide range of tools and flexibilities in your data visualization, allowing you much more freedom to build what you need.

Let's start by looking at the "in-site" reporting.

### 2.1. In-Site Reporting

#### 2.1.1. Home Screen

Both Adobe Analytics and Google Analytics provide a way to customize the first view a user sees when they log in.

##### 2.1.1.1. Workspace / Custom Set Home Screen (Adobe Analytics)

Adobe Analytics doesn't presume to create a pre-built report for all users to see on login. The default home page takes the user to the Workspace landing screen which will show each user all the workspace reports that they created or were shared with them. Also, each user has the ability to set any of these reports as their home screen if they so choose.

![image1](assets/ga-to-aa_1.png)

There will be more details below regarding workspace later on in this guide. See Section 2.1.2.1

>[!TIP]
>
>Create / Share some standard reports for your organization so that they have a starting point to see information without having to dive into building their own reports right away.



##### 2.1.1.2. Home Screen Insights (Google Analytics)

* Google Analytics Home Screen has some pre-built visualizations for you.  These cover things like:
* Users, Sessions, Bounce Rate, and Session Duration in the last 7 days
* Users by Time of Day in the last 30 days
* Current Users Right Now, and Top Active Pages
* Traffic Channel, Source/Medium, and Referrals in the last 7 days
* Sessions by Country in the last 7 days
* Top Pages for the Last 7 Days
* Active Users trend for the last 30 days
* and more

In GA4 users have more options to customize and add their own reports to the Home Screen.

![image2](assets/ga-to-aa_2.png)

This is probably the one thing you will miss most when coming to Adobe; they don't have such a home screen pre-built for you, but you can easily set up a custom Workspace to replicate what you need from the above and if you choose to, set it as your landing screen. More on this later (or see Section 2.1.2.1 Adobe Workspace).

#### 2.1.2. In-Site Report Builders

In addition to the Simple Reports that the analytics tools provided, each tool also provides more powerful tools with which to build out your own custom reports.

##### 2.1.2.1. Adobe Analytics Workspace

This is the powerhouse of Adobe Analytics, since its introduction in 2017 it has become the go to place for Analytics analysis, and the primary reason why the Reports section is soon-to-be sunset. 

This tool allows you to build out reports with almost complete freedom.

The report can be broken into Panels and those panels can contain any number of visualizations. Panels can be set to common information, such as date range and common segment filters.

Both the panels and the visualizations inside them can be resized and dragged around to show items side by side, or stacked. So if you wanted to compare two different suites of data side by side, you could create panels that split 50/50 down the middle showing the two sites side by side for easy comparison.

There are a multitude of visualizations available to users:

* Freeform Table
* Cohort Table
* Fallout
* Flow
* Graphs
  * Area (Stacked and Unstacked)
  * Line
  * Scatter
  * Bar (Stacked and Unstacked)
  * Bullet
  * Donut
  * Histogram
  * Horizontal Bar (Stacked and Unstacked)
* Map
* Summary Blocks
  * Summary Change
  * Summary Text
  * Text (free text field to enter extra information to give context)
* Venn

Each panel and visualization can be titled and have a description applied to it to help give context to what the information is showing.
In Adobe, segments (essentially filters for data) apply retroactively, and these can be pulled into columns of your freeform tables to compare data side by side. For instance, if a user wanted to compare two different categories on their site for traffic; they could create a segment for "Category A" and a different segment for "Category B".

![image3](assets/ga-to-aa_3.png)

Freeform tables allow for multiple columns and segmentation as is needed to visualize the data the way you want.

From the above, don't want to see a breakdown by date? Just drag and drop another dimension or segment there to see the data in a different way… like maybe using segments for Device Type, and then add a breakdown by OS for your Mobile/Tablet users:

![image3](assets/ga-to-aa_4.png)

Workspace allows your creativity to fly, you aren't limited to "standard" breakdowns. You can build out the visualizations that you need to deep dive into the comparisons you need to run.

>[!TIP]
>
>Don't be afraid to play and explore, there are so many ways to think outside the box here, see what you can do! But also, make sure you try to validate that what you have built is really showing what you think it is. Experience here will help!

You can even create on-the-fly calculated metrics or segments that live only inside the report (preventing flooding your segment and calculations repository, but also making sure that you can create focused items that are needed for specific reports without confusing your organization with things that aren't very usable in other contexts.

This discussion is just an introduction to this tool, there will be other more comprehensive guides to get you started, but when you do, you will be able to make comprehensive reports such as:

![image3](assets/ga-to-aa_5.png)

It should also be noted that Workspaces don't auto-save, so it's easier to do a one time ad-hoc report without clogging up your report repository.

Another powerful feature of workspaces is the ability to apply interactive modifiers to your reports in the form of drop-downs. While these drop-downs won't work on exported CSV or PDF files of your reports, within the live report they allow you to update all the visualizations in a panel to show the same report under different conditions. Multiple drop-downs can be used and so long as the options aren't mutually exclusive, the selected items will stack to allow for a clean way to present information.

>[!IMPORTANT]
>
>To read more about using drop-downs  and freeform breakdowns see <https://experienceleaguecommunities.adobe.com/t5/adobe-analytics-discussions/the-power-of-dropdown-filters-and-dimension-breakdowns-in-adobe/td-p/434680> 

##### 2.1.2.2. Google Analytics: Dashboards, Custom Reports and Saved Reports

Google has a few tools for creating reports within the interface, but they still follow the same display and limitations of the reports section. 

Now, for those versed in Google Analytics as you read this, you might be saying, "well wait a second, what about Google Data Studio, isn't that a better equivalent to Adobe's Workspace?" and you would be correct, but because Data Studio isn't technically a part of the Analytics tool, and allows for connections to different data sources, this tool is covered later in the "Extended Report Access" section of this discussion (and in particular Section 2.2.3)

Google Dashboards and Custom Reports allow you to pull multiple visualizations together into one report, but unlike Workspace, you are still locked into simple correlations and what data can be placed into what columns. 

In Custom Reports, one of the biggest challenges is the fact that when you create a filter it applies to all tabs of the report… there is no way to compare two different filters within the same report.

For surface comparisons it does the job. These are all similar to the Adobe Legacy Dashboards, Custom Reports and Bookmarks. Basic tools provided to support your needs, that reside within the report suite.

#### 2.1.3. Reports

Both Google and Adobe have some navigable reports that are per-built tables and basic timeline graphs based around a dimension.

##### 2.1.3.1. Adobe Analytics Reports

Adobe Analytics also has a Reports section, though in large this is mostly being phased out in favor of their Analysis Workspace (and in fact, end of life has been announced for this interface, since Workspace [Section 2.1.2.1] is a much more powerful tool), where most of these tables can be built and modified with more ease. Adobe's sections are far more broken out, and this can be daunting:

![image3](assets/ga-to-aa_6.png)

With most of the above being accessible via Workspaces, I will give a brief overview of these sections and how they relate to Google Analytics, and highlight the reports here that are still relevant.

Site Metrics is what you would expect, this covers the standard metrics (page views, unique visitors, visits, as well as custom events that you have set up). This is similar to the Behavior report GA, but also includes some of what you would find in Audience (since Adobe doesn't split up the metric types). 

In here you will also find "Bot" Reports, traffic from bots is excluded from all your standard reports, however, there are two reports that allow you to see some insight into what is happening and which bots are coming to your site. This is especially good if you set up custom Bot Rules to exclude known spammer bots that frequently hit your site. You can get some insight into what those bots are doing without your main reports being flooded but that traffic. Bot reports are currently unavailable through Workspace (but new reporting capabilities coming soon will allow users to get this information there as well).

Site Content is a grouping of Adobe standard dimensions: Page Name, Site Sections (Channels), Hierarchies (a way to create custom drill down reports of organization within your website), Servers (this is particularly helpful if you have multiple subdomains on your site, or are tagging multiple sites together into one tracking suite), etc. All of these are available in Workspace.

Mobile is a grouping of Mobile Device specific data, such as devices, device types, etc. All of these are available in Workspace.

Paths is another one of those "not quite available in Workspace" items… while Workspace does have a Flow diagram, you can only see the In and Out flows for a single page/value… whereas Paths allows you to see the most common paths used in your website. By default, Pages is the first path report that is set up for you, but you can turn this on for custom props (such as if you were to track a "Page Type" value, you could look at pathing within page types. The other thing that I personally like about Paths is the simple way the information is presented… The flow diagram in workspace (depending on how much you are trying to look at) can get overwhelming. I recommend trying both out… they each have a use and value depending on what you are trying to achieve. It should be noted that any dimension can be used in Flows, whereas Pathing must be set up on a Prop in the Admin panel.

Traffic Sources, Campaigns and Marketing Channels reports are all similar to the Acquisition report in Google. Traffic Sources focuses on Actual Referrers, Campaigns Focuses on your Campaign Codes, and Marketing Channels also focuses on Campaign Codes, but also applies extra logic as determined by you on how to process the information. I find that Adobe provides much more freedom on how to set up your rules, Google does a lot of stuff for you, and so that will be a bit of a shift in thinking. It should also be noted, that by default, Google's attribution on Campaign Codes is 6 months, Adobe's is set by default to 1 week. This can be changed in your admin settings, but in Workspace you can actually apply custom attribution on top of any dimension giving you much more "on-the-fly" flexibility.

Visitor Retention and Visitor Profile reports are similar to the Audience reports in Google Analytics. Retention is focused more on the return frequency, while Visitor Profile is focused more on the Geography and Technology of the users. 

Custom Conversion and Custom Traffic are both custom dimension reports, Conversions are your eVars (where you can set a custom expiry to the value - i.e. hit, visit, month, year, etc… and this value will remain for that user for the specified time unless overwritten). Traffic variables are your props, but you can also set these up for Pathing Reports, or as list items (that will break apart multiple values based on a delimiter of your choice).

Media is for things like Videos or Audio files where you have set up special media tracking.

Custom Reports is a section where a user can customize the columns and breakdowns that they have created within the reports interface and save it as a custom report. However, as mentioned above, since Workspace allows for so much more powerful breakdowns and correlations, anything customized should just be made there. This was a good solution back before Workspace existed.

The Bookmarks section is similar to Custom Reports, where frequently used reports could be bookmarked within the reports interface so that they could be found easier.

Dashboard was a legacy product that allowed people to combine reportlets of data together into one visualization. However, the functionality in Workspace (Section 2.1.2.1) is so much easier to work with, that this only exists as an access point to legacy reports that should be rebuilt before this feature is sunset.

Targets is a special report area that allows people to create a report based on a target within a certain timeframe so that teams could monitor things like campaigns and see if they were on track to hit their traffic targets.

All the reports here allowed for multiple metric columns and dimension breakdowns. but the simplicity of the visualizations and some of the logic behind what elements could be correlated could be frustrating at times.

##### 2.1.3.2. Google Analytics Reports

Google Analytics splits these reports into the following sections: Realtime, Audience, Acquisition, Behavior and Conversations (in GA3) and into Lifecycle (with the subsections: Acquisition, Engagement, Monetization, Retention) and User (with the subsections: Demographics and Tech).

![image3](assets/ga-to-aa_7.png)

You can make some minor tweaks to these visualizations, add a secondary dimension breakdown, change the visualization, create a filter on the data, etc. You can save your customizations as a Saved Report.

These give you quick and easy insights to your data. However, you can't compare things like Users to page views for a page in the same table, and you can't add more than one extra dimension to see additional data. 

These are good for quick analytical data, but if you really need to dig deep, they suffer from the limitations.

### 2.2. Extended Report Access

In addition to "In-Site Reporting", most tools offer extended functionality that allow you to take your analysis outside of the tools and build something a little more customized.

#### 2.2.1. Adobe Analytics Report Builder (Microsoft Excel Extension)

Workspace is a great tool, but sometimes you need to get your data into a customized spreadsheet, possibly so that you can stitch together multiple sources of data. This is where Report Builder comes into play.

Report Builder is a plug-in for Microsoft Excel that allows you to create connections to your Adobe Analytics data to pull in tabular data that you can manipulate within Excel. Generally to use this efficiently you would pull the data into some raw data tabs, then use excel cell references to pull data from these tabs into a single consolidated report, then create graphs and visualizations.

>[!NOTE]
>
>Report Builder has a special permission that needs to be applied to your users to access this plugin. This should probably only be granted to users who have learned how to use the tool properly.

#### 2.2.2. Adobe Analytics API Connection

If you need your Adobe Analytics to be digested by something other than excel, but you still want the benefits of processed data (including the bot rule exclusions), you can use Adobe's API to pull data out directly, then process it via script or add it to a database for use with another system.

It should be noted that the API still pulls in correlation data applying the breakdowns and segments as are specified in the pull request. 

Adobe's Workspace (Section 2.1.2.1) actually uses the API to build all of the reports, and if you enable debug mode in Workspace, it will show you the exact API calls used. This is a quick way to build out your API calls by using Workspace to build and validate the data you want to pull, then use those API calls to get the data out to your own processing.


#### 2.2.3. Google Analytics Data Studio

If you have been reading along, you will already know from above that I mentioned Data Studio as being an equivalent to Adobe's Workspace. Data Studio allows you to pull in Google Analytics data, but also data from other sources. This is nice if you want to consolidate your analytics data with other collected data; but when it comes to Google Analytics, I have found the same sort of visualization limitations that are present in Google Analytics. The way the rows and columns are formed are still very limited in what can be done. 

It's still a powerful tool, and I wouldn't dissuade people from using it in any way, but my personal experience is that having used Workspace for so long, I personally find the rigid behavior quite limiting.


#### 2.2.4. Google Spreadsheet Extension

For my own uses, when I need to pull data in an extended manner from Google Analytics, my personal tool of choice is the Google Spreadsheet Extension. Sure, I need to make multiple connections to my GA tables, but like Adobe's Report Builder, I can reference the cells from the raw data and build out the reports I need, then visualize them using the graphing capabilities of Google Spreadsheet.


## 3. Raw Data Exports

For those times you really need raw data, both Adobe and Google offer the capabilities to pull information in this manner.

### 3.1. Adobe Data Feed

In Section 2.2.2, I mentioned that the Adobe Analytics API pulled from "processed data". The Raw Data feed will still pull data processed by the "Processing Rules" that have been set up in the admin panel (make sure that your raw data is delayed to ensure all these rules have completed by the time the raw data feed is pulled), but this raw data will include all the data that is excluded everywhere else.

This means that all your Bot exclusions, internal IP filtered data, etc will be included in the raw data feeds. There are flags to identify this data, so that if you are building a data lake, your engineering team can create logic to process this data accordingly.

The raw data feeds can be customized to send all the columns of data, or only specific columns if you need a more focused feed.

The feeds can be sent directly to FTP, SFTP, S3, etc.


### 3.2. Google Big Query

Unfortunately, this is one Google Tool I have not had any experience using, but in theory it should be similar to Adobe's Data Feed, allowing your engineering team to access raw data from your Google Analytics account.

However, I believe rather than a full dump of raw data, it allows your engineers to access the data via SQL queries, so they can pull either targeted raw data or if they wish they could pull all columns of raw data to ingest into a data lake. 

## 4. Conclusion

Like any system, practice is needed to get comfortable with it, but hopefully this guide will get you started, or give you tips to improve your usage of Adobe Analytics if you have only scratched the surface. 

I will, however, stress that I would recommend using both Adobe Analytics and Google Analytics in your implementation strategy (even if the Google Analytics is only the free version). This allows you to have a backup system to ensure you have data, as no system is infallible.

There are many resources available to you beyond this guide that can help improve your strategy:

* [Adobe Experience League](https://experienceleague.adobe.com/#home) (which contains tutorials, videos, documentation, and community forums
* [Adobe User Groups](https://analytics-augs.adobe.com/) (this is a hub of community run events to help users connect with each other and improve their implementations - just because these are based in certain time zone, it's best to check what other regions are running as well)
* YouTube Channel
  * [Adobe Analytics User Groups](https://www.youtube.com/channel/UCQOHnCs7KZgsuFHVzwboQuA)
* Slack Channels
  * [Measure Chat](https://www.measure.chat/)
* and more

## Author

This document was written by:

![Jennifer Dugan](assets/Jennifer_Dungan_Headshot150.png)

Jennifer Dugan, Optimization Manager Analytics at Torstar
