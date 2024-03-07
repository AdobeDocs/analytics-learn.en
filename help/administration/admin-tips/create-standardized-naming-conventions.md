---
title: Create standardized naming conventions
description: Standardized Naming conventions apply to both the variable name itself when enabled in the AA Admin UI and the values passed into the dimension.
feature: Implementation Basics
topic: Administration
role: Admin
level: Beginner
doc-type: article
thumbnail: 10531.jpg
kt: 10531
exl-id: 0fe3b981-0d9b-4f12-a6ca-63a4140f4baf
---
# Create standardized naming conventions

**WHAT:** Standardized naming conventions apply to both the variable name itself when enabled in the Adobe Analytics (AA) admin UI and the values passed into the dimension. (i.e. page names would be "page name (v1)" as a variable name and the page name values passed in should be uniform and follow a specific structure/hierarchy like "sitename|homepage" or "sitename|search|searchresults").

**WHY:** Naming conventions are a great way to keep everything uniform and keep the interface easy to understand for your users. If you create these from the start and enforce them in the platform and the code, these will be easier to scale.

**HOW:** The interface and tagging doc should match for both 'Name' and 'Description' - this will save your users from having to pull up an Excel doc and allow them to understand your data directly in the interface. It is also recommended to keep everything lower case for consistency.

It's always best to keep page names consistent across the platform as well (or screen names for apps). For example, you can set `property:section:sub section:sub sub section:unique page name` into a variable/dimension. If all of these are separate fields in your data layer, you could even build the page name directly in your JS file/Launch. Having all these elements set in their own dimensions as well can help you to break down specific properties or areas of your site/app more easily, and better understand traffic and flows.

Anything that makes it easier for users to find and understand the data, including something as simple as naming conventions, will increase the usage of Adobe Analytics and deliver better insights for the business.

## Authors

This document was co-written by:

![Christel Guidon](assets/Christel-Headshot-150.png)

Christel Guidon, Digital Analytics Platform Manager at NortonLifeLock
Adobe Analytics Champion

![Rachel Fenwick](assets/Rachel-Fenwick-150.png)

Rachel Fenwick, Senior Consultant at Adobe
