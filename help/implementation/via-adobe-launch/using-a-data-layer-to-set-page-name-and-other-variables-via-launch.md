---
title: Using a Data Layer to set Page Name and Other Variables in Adobe Analytics via Launch
seo-title: Using a Data Layer to set Page Name and Other Variables in Adobe Analytics via Launch
description: Using a data layer for Analytics and other Experience Cloud solutions is considered a best practice. In this video, you’ll see how to pull your values out of the data layer and use them in Launch to populate variables in Adobe Analytics.
seo-description: Using a data layer for Analytics and other Experience Cloud solutions is considered a best practice. In this video, you’ll see how to pull your values out of the data layer and use them in Launch to populate variables in Adobe Analytics.
uuid: 62352c19-8cc4-430a-bc04-732adb258559
products: SG_ANALYTICS
discoiquuid: a48afea2-db29-4a15-9756-d4418ee9ae88
targetaudience: target-audience new;target-audience ongoing
index: y
internal: n
snippet: y
---

# Using a Data Layer to set Page Name and Other Variables in Adobe Analytics via Launch {#using-a-data-layer-to-set-page-name-and-other-variables-in-adobe-analytics-via-launch}

Using a data layer for Analytics and other Experience Cloud solutions is considered a best practice. In this video, you’ll see how to pull your values out of the data layer and use them in Launch to populate variables in Adobe Analytics.

## Data Layers {#data-layers}

It is a best practice to use a data layer when working with data on your site and Adobe Experience Cloud solutions, especially with Adobe Analytics. A "data layer" is a framework of JavaScript objects that developers insert into pages. The data layers can be used by tracking tools (including tag management systems like Adobe Launch) to populate reports. Find additional information about data layers in the [Experience Cloud documentation](https://marketing.adobe.com/resources/help/en_US/sc/implement/ref-data-layer.html) or on the [W3C site](https://www.w3.org/).

In addition, please reference the blog post [“Data Layers: From Buzzword to Best Practice,”](https://theblog.adobe.com/data-layers-buzzword-best-practice/) which will give you some great info about data layers, as well as a couple of examples.

## Data Layers, Launch, and Adobe Analytics (oh my?) {#data-layers-launch-and-adobe-analytics-oh-my}

1. Create a data layer standard to use on your site, which can be referenced by Adobe Launch

    1. Put this data layer as high as possible in the head of the page, before the call to Adobe Launch, so that the values can be used immediately by Launch, and by Adobe solutions that need to be high on the page, like Adobe Target

1. Populate the data in the data layer
1. In Launch, create “data elements” that reference the data points in the data layer, and which can be used throughout Launch in rules, extensions, etc.
1. Use the data elements in either the Analytics extension global variables or in a rule, assigning the values into props, eVars, pageName, or other Analytics variables
1. Trigger a beacon that sends the data into Analytics

The following video will walk you through the process.

>[!VIDEO](https://video.tv.adobe.com/v/25899/?quality=12)