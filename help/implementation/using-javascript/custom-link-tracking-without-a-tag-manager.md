---
title: Custom Link Tracking without a Tag Manager
seo-title: Custom Link Tracking without a Tag Manager - Adobe Analytics
description: For many actions on the page, tracking should not be treated like a page view. In this video, you will learn how to code a link tracking beacon to Analytics, if you are not using a tag manager (like Adobe Launch). See the code, as well as learning an important tip.
seo-description: For many actions on the page, tracking should not be treated like a page view. In this video, you will learn how to code a link tracking beacon to Analytics, if you are not using a tag manager (like Adobe Launch). See the code, as well as learning an important tip. - Adobe Analytics
uuid: 5c28a488-6e8b-439a-86cf-dc1035a17dbd
discoiquuid: 7c947643-0861-4827-95ad-65f0cb7c53af
feature: implementation - using javascript
topics: 
audience: implementer
activity: implement
doc-type: technical video
author: Doug Moore
team: Technical Marketing
kt: 1845
---

# Custom Link Tracking without a Tag Manager {#custom-link-tracking-without-a-tag-manager}

For many actions on the page, tracking should not be treated like a page view. In this video, you will learn how to code a link tracking beacon to Analytics, if you are not using a tag manager (like Adobe Launch). See the code, as well as learning an important tip.

## Sending an s.tl() Beacon {#sending-an-s-tl-beacon}

There are two functions that send data into Adobe Analytics:

1. s.t() - A “track” beacon, which is a page view hit, incrementing page views for the given page name, as well as setting other variables
1. s.tl() - a “track link” beacon, which is often referred to as a “custom link” hit/beacon, which does not increment page views, and ignores the pageName variable. This is commonly used for tracking smaller actions on the page that don’t load a new page/screen, or other actions that don’t result in a new page load.

**Note:** As stated in the title of this page, in this video we are showing you how to code a custom link hit when you are NOT using a tag manager, like Adobe Launch. We still do recommend that you use Adobe Launch, our best practice recommendation for implementation. However, if you are not using Adobe Launch and need to code in an s.tl(), here’s how to do it.

>[!VIDEO](https://video.tv.adobe.com/v/25832/?quality=12)

## Sample Code {#sample-code}

Here is the sample code used on the custom link in the video:

**&lt;a href="#" onclick="
    s.linkTrackVars='events,eVar2,prop2';
    s.linkTrackEvents=s.events='event2';
    s.eVar2='facebook share';
    s.prop2='facebook share';
    s.tl(this,'o','Social Share');
    s.manageVars('clearVars',s.linkTrackVars,1);
"&gt;Click here to share on FaceBook
&lt;/a&gt;**

For more information on custom links, please see the [documentation](https://marketing.adobe.com/resources/help/en_US/sc/implement/function_tl.html).