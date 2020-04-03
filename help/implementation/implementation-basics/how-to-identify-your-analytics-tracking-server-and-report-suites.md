---
title: How to Identify Your Analytics Tracking Server and Report Suites
description: When setting up Adobe Analytics, or when referencing it in other Experience Cloud solutions, it is often helpful or even necessary to know the Analytics “Tracking Server” that you are using, or also the “Report Suite” that you are sending data into. This video shows you how to locate both values, whether or not you have already implemented Adobe Analytics.
feature: implementation basics
topics: 
audience: implementer
activity: implement
doc-type: technical video
team: Technical Marketing
kt: 2358
---

# How to Identify Your Analytics [!DNL Tracking Server] and [!UICONTROL Report Suites] {#how-to-identify-your-analytics-tracking-server-and-report-suites}

When setting up Adobe Analytics, or when referencing it in other Experience Cloud solutions, it is often helpful or even necessary to know the [!DNL Analytics] “[!DNL Tracking Server]” that you are using, or also the “[!UICONTROL Report Suite]” that you are sending data into. This video shows you how to locate both values, whether or not you have already implemented Adobe Analytics.

## After Implementation {#after-implementation}

After implementing [!DNL Analytics] on a site, you can find the [!DNL tracking server] and the [!DNL report suite ID] right in the tracking beacon. The [!DNL tracking server] is the hostname in the beacon, so that’s easy to find. The [!UICONTROL report suite] IDs are a comma-separated list right after “/b/ss/” in the path name of the beacon.

To see the beacon, as well as all other information coming to [!DNL Analytics] and other Experience Cloud solutions, install the [“Experience Cloud Debugger” Chrome Extension](https://chrome.google.com/webstore/detail/adobe-experience-cloud-de/ocdmogmohccmeicdhlhhgepeaijenapj?hl=en).

## Before Implementation {#before-implementation}

**[!DNL Tracking Server]** - If you haven’t started with your Adobe Analytics implementation yet, then you will choose a subdomain for the “.sc.omtrdc.net” [!DNL tracking server]. For example, let’s say that I have an online hat store called “Jim’s Brims.” I can simply set my [!DNL tracking server] to:

“jimsbrims.sc.omtrdc.net”.

**[!UICONTROL Report Suite]** - To find a list of your [!UICONTROL report suites] that have been created, log into [!DNL Analytics] and go to [!UICONTROL Admin] &gt; [!UICONTROL Report Suites] in the top menu to see a list of [!UICONTROL report suites], including their ID and title.

See the video below for more information.

>[!VIDEO](https://video.tv.adobe.com/v/26061/?quality=12)
