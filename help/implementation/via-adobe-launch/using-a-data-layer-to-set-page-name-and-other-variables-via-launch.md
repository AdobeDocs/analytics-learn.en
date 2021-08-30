---
title: Using a Data Layer to set Page Name and Other Variables in Adobe Analytics via Launch
description: Using a data layer for Analytics and other Experience Cloud solutions is considered a best practice. In this video, you’ll see how to pull your values out of the data layer and use them in Launch to populate variables in Adobe Analytics.
feature: Launch Implementation
topics: 
activity: implement
doc-type: technical video
team: Technical Marketing
kt: 1852
role: Developer, Data Engineer
level: Beginner
exl-id: 408ceb47-df05-4456-85bb-0ef2798a05a5
---
# Using a Data Layer to set Page Name and Other Variables via [!DNL Experience Platform Launch] {#using-a-data-layer-to-set-page-name-and-other-variables-in-adobe-analytics-via-launch}

Using a data layer for [!DNL Analytics] and other Experience Cloud solutions is considered a best practice. In this video, you’ll see how to pull your values out of the data layer and use them in [!DNL Experience Platform Launch] to populate variables in Adobe Analytics.

## Data Layers {#data-layers}

It is a best practice to use a data layer when working with data on your site and Adobe Experience Cloud solutions, especially with Adobe Analytics. A _data layer_ is a framework of JavaScript objects that developers insert into pages. The data layers can be used by tracking tools (including tag management systems like [!DNL Experience Platform Launch]) to populate reports. Find additional information about data layers in the [Experience Cloud documentation](https://experienceleague.adobe.com/docs/analytics/implementation/prepare/data-layer.html?lang=en) or on the [W3C site](https://www.w3.org/).

In addition, see the blog [Data Layers: From Buzzword to Best Practice,](https://theblog.adobe.com/data-layers-buzzword-best-practice/), which gives you some great information about data layers, as well as a couple of examples.

## Data Layers, [!DNL Experience Platform Launch], and Adobe Analytics (oh my?){#data-layers-launch-and-adobe-analytics-oh-my}

1. Create a data layer standard to use on your site, which can be referenced by [!DNL Experience Platform Launch].

    1. Put this data layer as high as possible in the head of the page, before the call to [!DNL Experience Platform Launch], so that the values can be used immediately by [!DNL Launch], and by Adobe solutions that need to be high on the page, like Adobe Target.

1. Populate the data in the data layer.
1. In [!DNL Experience Platform Launch], create “[!UICONTROL data elements]” that reference the data points in the data layer, and which can be used throughout [!DNL Experience Platform Launch] in [!UICONTROL rules], [!UICONTROL extensions], and so on.
1. Use the [!UICONTROL data elements] in either the [!DNL Analytics] extension global variables or in a rule, assigning the values into [!UICONTROL props], [!UICONTROL eVars], [!UICONTROL pageName], or other [!DNL Analytics] variables.
1. Trigger a beacon that sends the data into [!DNL Analytics].

The following video walks you through the process.

>[!VIDEO](https://video.tv.adobe.com/v/25899/?quality=12)
