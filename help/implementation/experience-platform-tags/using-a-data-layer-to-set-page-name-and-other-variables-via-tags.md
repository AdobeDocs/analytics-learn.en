---
title: Use a data layer to set Analytics variables in Experience Platform [!DNL tags]
description: Learn how to use a data layer for sourcing Analytics data and other Experience Cloud solutions. 
feature: Tags
topics: Development
role: Developer, Data Engineer
level: Beginner
kt: 1852
thumbnail: 25899.jpg
exl-id: 408ceb47-df05-4456-85bb-0ef2798a05a5
---
# Use a data layer to set Analytics variables in Experience Platform [!DNL tags]

Using a data layer for [!DNL Analytics] and other Experience Cloud solutions is a best practice. In this video, learn how to pull values out of the data layer and use them in Experience Platform [!DNL tags] to populate variables in Adobe Analytics.

## Data layers 

A _data layer_ is a framework of JavaScript objects that developers add to digital web pages. Analytics solutions ultimately use the data layer to populate reports. Tag management systems, including Experience Platform [!DNL tags]) are the intermediaries that read the data layer, map the values to variables, and send that data to digital experience solutions. 

Review additional information about data layers in the [Experience Cloud documentation](https://experienceleague.adobe.com/docs/analytics/implementation/prepare/data-layer.html?lang=en).

## Data Layers, Experience Platform [!DNL tags], and Adobe Analytics

1. Define or identify a data layer standard to use on your site. 

    1. Position the data layer as high as possible in the head section of the page and before the call to Experience Platform [!DNL tags]. This ensures that the values are accessed immediately by [!DNL tags] and by Adobe solutions that need to be high on the page, like Adobe Target.

1. Populate the data in the data layer.
1. In Experience Platform [!DNL tags], create "[!UICONTROL data elements]" that map the data points in the data layer. These data elements are used throughout Experience Platform [!DNL tags] in [!UICONTROL rules] and [!UICONTROL extensions].
1. In either the [!DNL Analytics] extension's global variables section or in a [!DNL Tags rule], assign the values in [!UICONTROL data elements] to [!UICONTROL props], [!UICONTROL eVars], [!UICONTROL pageName], and other [!DNL Analytics] variables.
1. Trigger a beacon that sends the data into [!DNL Analytics].

The following video walks you through the process.

>[!NOTE]
>
> Launch is now **[!DNL tags]**

>[!VIDEO](https://video.tv.adobe.com/v/25899/?quality=12&learn=on)

>[!NOTE]
>
>The specific data layer used in this video may not be considered "best practice" for your organization. The concept of using a data layer for surfacing important data to your digital marketing solutions is best practice.
