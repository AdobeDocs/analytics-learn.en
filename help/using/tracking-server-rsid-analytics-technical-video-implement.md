---
title: How to Identify Your Analytics Tracking Server and Report Suites
seo-title: How to Identify Your Analytics Tracking Server and Report Suites
description: When setting up Adobe Analytics, or when referencing it in other Experience Cloud solutions, it is often helpful or even necessary to know the Analytics “Tracking Server” that you are using, or also the “Report Suite” that you are sending data into. This video shows you how to locate both values, whether or not you have already implemented Adobe Analytics.
seo-description: When setting up Adobe Analytics, or when referencing it in other Experience Cloud solutions, it is often helpful or even necessary to know the Analytics “Tracking Server” that you are using, or also the “Report Suite” that you are sending data into. This video shows you how to locate both values, whether or not you have already implemented Adobe Analytics.
uuid: 1a7f7e49-3750-4608-baa6-f4b9eacde6d5
products: SG_ANALYTICS
discoiquuid: 58ce44a1-89e9-447a-baa9-4293a13380e4
targetaudience: target-audience new;target-audience ongoing
index: y
internal: n
snippet: y
---

# How to Identify Your Analytics Tracking Server and Report Suites{#how-to-identify-your-analytics-tracking-server-and-report-suites}

## After Implementation {#after-implementation}

After implementing Analytics on a site, you can find the tracking server and the report suite ID right in the tracking beacon. The tracking server is the hostname in the beacon, so that’s easy to find. The report suite IDs are a comma-separated list right after “/b/ss/” in the path name of the beacon.

To see the beacon, as well as all other information coming to Analytics and other Experience Cloud solutions, install the [“Experience Cloud Debugger” Chrome Extension](https://chrome.google.com/webstore/detail/adobe-experience-cloud-de/ocdmogmohccmeicdhlhhgepeaijenapj?hl=en).

## Before Implementation {#before-implementation}

**Tracking Server** - If you haven’t started with your Adobe Analytics implementation yet, then you will choose a subdomain for the “.sc.omtrdc.net” tracking server. For example, let’s say that I have an online hat store called “Jim’s Brims.” I can simply set my tracking server to:

“jimsbrims.sc.omtrds.net”.

**Report Suite** - To find a list of your report suites that have been created, log into Analytics and go to Admin &gt; Report Suites in the top menu to see a list of report suites, including their ID and title.

See the video below for more information.

>[!VIDEO](https://video.tv.adobe.com/v/26061/?quality=12)

