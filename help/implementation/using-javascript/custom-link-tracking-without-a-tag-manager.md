---
title: Custom Link Tracking without a Tag Manager
description: For many actions on the page, tracking should not be treated like a page view. In this video, you will learn how to code a link tracking beacon to Analytics, if you are not using a tag manager (like Experience Platform Launch). See the code, as well as learning an important tip.
feature: Appmeasurement Implementation
topics: null
activity: implement
doc-type: technical video
team: Technical Marketing
kt: 1845
role: Developer
level: Intermediate
exl-id: e4567b1c-414e-44ad-982f-52b0150e7eda
TQID: https://experienceleague.adobe.com/BU98KM1JAq3v6Gd7SRU0FNT3qW-4a9UvP0M-ffFqJIA
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
    internal-label: Measurement
---
# Custom Link Tracking without a Tag Manager {#custom-link-tracking-without-a-tag-manager}

For many actions on the page, tracking should not be treated like a page view. In this video, you will learn how to code a link tracking beacon to Analytics, if you are not using a tag manager (like Adobe [!DNL Experience Platform Launch]). See the code, as well as learning an important tip.

## Sending an s.tl() Beacon {#sending-an-s-tl-beacon}

There are two functions that send data into Adobe Analytics:

1. s.t() - A “track” beacon, which is a page view hit, incrementing page views for the given page name, as well as setting other variables
1. s.tl() - a “track link” beacon, which is often referred to as a “custom link” hit/beacon, which does not increment page views, and ignores the pageName variable. This is commonly used for tracking smaller actions on the page that don’t load a new page/screen, or other actions that don’t result in a new page load.

>[!NOTE]
>
>In this video, we show you how to code a custom link hit when you are NOT using a tag manager like Adobe [!DNL Experience Platform Launch]. We recommend that you use [!DNL Experience Platform Launch], our best-practice recommendation for implementation. However, if you need to code in an `s.tl()`, here’s how to do it.

>[!VIDEO](https://video.tv.adobe.com/v/25832/?quality=12&learn=on)

## Sample Code {#sample-code}

Here is the sample code used on the custom link in the video:

```JavaScript
<a href="#" onclick="
    s.linkTrackVars='events,eVar2,prop2';
    s.linkTrackEvents=s.events='event2';
    s.eVar2='facebook share';
    s.prop2='facebook share';
    s.tl(this,'o','Social Share');
    s.manageVars('clearVars',s.linkTrackVars,1);">
    Click here to share on FaceBook
</a>
```
