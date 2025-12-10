---
title: How to identify your analytics tracking server and report suite ID
description: When setting up Adobe Analytics, or when referencing it in other Experience Cloud solutions, it is often helpful or even necessary to know the Analytics "Tracking Server" that you are using, or also the "Report Suite" that you are sending data into. This video shows you how to locate both values, whether or not you have already implemented Adobe Analytics.
feature: Implementation Basics
topics: 
activity: implement
doc-type: technical video
team: Technical Marketing
kt: 2358
role: Developer
level: Beginner
exl-id: 3925026f-69f1-4425-b3a9-6fef26375fed
---
# How to identify your analytics [!DNL tracking server] and [!UICONTROL report suite ID] {#how-to-identify-your-analytics-tracking-server-and-report-suites}

When setting up Adobe Analytics, or when referencing it in other Experience Cloud solutions, it is often helpful or even necessary to know the Analytics "tracking server" that you are using, or also the "[!UICONTROL report suite]" that you are sending data into. This video shows you how to locate both values, whether or not you have already implemented Adobe Analytics.

>[!IMPORTANT]
>
>This article and video apply to an "AppMeasurement" implementation of Adobe Analytics, and not an implementation using the Web SDK.

## After implementation {#after-implementation}

After implementing Analytics on a site, you can find the [!DNL tracking server] and the [!DNL report suite ID] right in the tracking beacon. The [!DNL tracking server] is the hostname in the beacon, so that's easy to find. The [!UICONTROL report suite] IDs are a comma-separated list right after "/b/ss/" in the path name of the beacon.

To see the beacon, as well as all other information coming to Analytics and other Experience Cloud solutions, install the ["Experience Cloud Debugger" Chrome Extension](https://chrome.google.com/webstore/detail/adobe-experience-cloud-de/ocdmogmohccmeicdhlhhgepeaijenapj?hl=en).

## Before Implementation {#before-implementation}

**[!DNL Tracking server]** - If you haven't started with your Adobe Analytics implementation yet, then you will choose a subdomain for the ".sc.omtrdc.net" [!DNL tracking server]. For example, let's say that I have an online hat store called "Jim's Brims." I can simply set my [!DNL tracking server] to:

"jimsbrims.sc.omtrdc.net".

**[!UICONTROL Report suite]** - To find a list of your [!UICONTROL report suites] that have been created, log into [!DNL Analytics] and go to [!UICONTROL Admin] &gt; [!UICONTROL Report Suites] in the top menu to see a list of [!UICONTROL report suites], including their ID and title.

See the video below for more information.

>[!VIDEO](https://video.tv.adobe.com/v/26061/?quality=12&learn=on)
