---
title: Use a global report suite
description: Having a single global report suite can help in many ways, and really simplify your implementation.
feature: Implementation Basics
topic: Administration
role: Admin
level: Beginner
doc-type: article
thumbnail: 10536.jpg
kt: 10536

---

# Use a global report suite

**WHAT:** It's tempting to create report suites for each of your sites, but this can quickly become your worst nightmare - both in terms of complicating your reporting as well as your implementation. Having a single global report suite can help in many ways, and really simplify your implementation. 

**WHY:** Creating a global report suite is your only option for having a unified view of your digital properties and users' journeys across each property. If you have a mobile app and website, you should always combine the app data and web data in one report suite to take advantage of cross device journeys and track those who visit both properties as a single visitor vs. with separate report suites, where you would have a disjointed data set showing 2 visitors - 1 to each property - with no way of knowing the crossover. 

Here are the advantages/disadvantages of having a single report suite to help you weigh your options:

* PROS:
    * Being able to understand your entire digital landscape easily. If you implemented the 'properties' dimension (eVar) referenced in other tips, you will be very easily able to get a single view of all your sites & apps, traffic, and conversions. Having this big picture view is key to understanding your business overall.
    * In the same sense, you can now see how users flow across all your properties and understand their journey throughout your digital landscape.
    * Ease of administering. When using multiple report suites, you will need to maintain the interface in several places, as well as several tagging docs (or a more complicated one). Keeping everything in one place means there's only one place to make updates. It also makes granting access a lot easier as well.
    * Better usability in the interface. If your users only have one place to go, they don't need to think about which report suite to select. Keep in mind that you can't use multiple report suites within the same workspace panel, and having several of them can confuse your users.
    * Fewer server calls = fewer costs. If you make calls to multiple report suites, you increase your costs. Keeping your implementation simple will also keep your costs down.
    * You can simply leverage virtual report suites (VRS) to break out site-specific data within the global report suite and narrow user permissions based on a VRS if needed. Once data is separated into individual report suites, you cannot roll it up, but if it is already joined in one dataset (global RS), it is easily broken down.
* CONS:
    * If you have very separate properties where users don't cut over from one to the other and are never expected to do so, you may want to maintain separate report suites. 
    * If your properties have vastly different tagging and reporting needs, it can make sense to set up separate report suites in the interest of variable efficiency. Having separate report suites will give you more flexibility in using custom variables (more eVars).
    * Uniques exceeded: The Adobe Analytics interface only allows you to see 500,000 unique values within a single dimension for a given time period. Once you exceed this, values will be grouped as 'uniques exceeded' or 'low traffic' in the interface. These values do remain available to you on the backend (i.e. Data Warehouse, Data Feeds), but cannot be visualized within the interface. If you have very granular data (such as User ID, PSN, etc.), it's easy to reach this level. Having separate report suites can help with this issue.

**HOW:** Starting with a new AA implementation and using one global report suite is simple and straightforward. You would just need to create the global report suite (one for Dev and one for Prod) in the AA admin UI and apply the same report suite ID (RSID) values across all of your properties. 

Migrating from a multi-tagging strategy with a unique report suite per property requires more strategy and planning. A few of the considerations you will need to keep in mind:

* Aligning your variables (i.e. eVar1 on Property A needs to be capturing the same data point as eVar1 on Property B)
* Consolidating any processing rules, marketing channel rules, classifications (SAINT and Rule Builder)
* Migrating any Data Feeds and Data Sources 
* Choosing a cut over date and communicating this with all business users 

## Authors

This document was co-written by:

![Christel Guidon](assets/Christel-Headshot-150.png)

Christel Guidon, Digital Analytics Platform Manager at NortonLifeLock
Adobe Analytics Champion

![Rachel Fenwick](assets/Rachel-Fenwick-150.png)

Rachel Fenwick, Senior Consultant at Adobe
