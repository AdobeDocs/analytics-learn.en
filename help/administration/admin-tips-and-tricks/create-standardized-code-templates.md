---
title: Create standardized code templates
description: For a baseline implementation (i.e. what your company considers the must-have KPIs for all Adobe Analytics sites), your org should have a single implementation method where possible. 
feature: Implementation Basics
topic: Administration
role: Admin
level: Beginner
doc-type: article
thumbnail: 10532.jpg
kt: 10532

---

# Create standardized code templates

**WHAT:** For a "baseline" implementation (i.e. what your company considers the must-have KPIs for all Adobe Analytics sites), your org should have a single implementation method where possible. For instance, use the same data layer structure across sites and leveraging the same tag manager rule/custom code to capture things like internal searches or visitor profile information.

**WHY:** Having a repeatable and scalable baseline implementation makes adding new elements or new sites/apps a streamlined, low effort endeavor while also keeping your implementation clean and easy to troubleshoot. Using a uniform method also makes it easier for new admins/developers to come online and understand what they are working with.

**HOW:** Adopt a single format template to hand off to developers when a new site or tagging enhancement comes online. Typically, a word doc works well where you can outline the following items: 

* Variables being implemented, their purpose, and when to set. For example:

| AA Variable | Description | When/Where to Set | How to Set |
|--- |--- |--- |--- |
| eVar8	| Internal Search Keywords	| On landing of internal search results page | data layer |
| event8 | Count of Internal Searches | On landing of internal search results page | Launch rule |

* Detail around how to set. This is where you would specify any data layer objects needed and their syntax as well as any TMS rules that need to be configured and the details of the rule setup.
* Test cases to ensure are covered in the QA and all variables you expect to see in a successful test case. Outline what a successful implementation should include when the developer tests this enhancement.

Ideally, this document will only need to be tweaked for the next site where you update the basics like property name, page naming convention, etc. No need to reinvent the wheel each time, and you can save more time.

## Authors

This document was co-written by:

![Christel Guidon](assets/Christel-Headshot-150.png)

Christel Guidon, Digital Analytics Platform Manager at NortonLifeLock
Adobe Analytics Champion

![Rachel Fenwick](assets/Rachel-Fenwick-150.png)

Rachel Fenwick, Senior Consultant at Adobe
