---
title: Use a data layer to set Analytics variables via Tags
description: Learn about using a data layer for sourcing Analytics data and other Experience Cloud solutions. 
feature: Launch Implementation
role: Developer, Data Engineer
level: Beginner
kt: 1852
thumbnail: 25899.jpg
exl-id: 408ceb47-df05-4456-85bb-0ef2798a05a5
---
# Use a data layer to set Analytics variables via [!DNL Tags] {#use-a-data-layer-to-set-analytics-variables-in-adobe-analytics-via-tags}

Using a data layer for [!DNL Analytics] and other Experience Cloud solutions is a best practice. In this video, learn how to pull values out of the data layer and use them in [!DNL Experience Platform Tags] to populate variables in Adobe Analytics.

## Data layers {#data-layers}

A _data layer_ is a framework of JavaScript objects that developers add to digital web pages. Analytics solutions ultimately use the data layer to populate reports. Tag management systems, including [!DNL Experience Platform Tags]) are the intermediaries that read the data layer, map the values to variables, and  send that data to digital experience solutions. 

Review additional information about data layers in the [Experience Cloud documentation](https://experienceleague.adobe.com/docs/analytics/implementation/prepare/data-layer.html?lang=en).

## Data Layers, [!DNL Experience Platform Tags], and Adobe Analytics{#data-layers-launch-and-adobe-analytics}

1. Define or identify a data layer standard to use on your site. 

    1. Position the data layer as high as possible in the head section of the page and before the call to [!DNL Experience Platform Tags]. This ensures that the values are accessed immediately by [!DNL Tags] and by Adobe solutions that need to be high on the page, like Adobe Target.

1. Populate the data in the data layer.
1. In [!DNL Experience Platform Tags], create "[!UICONTROL data elements]" that map the data points in the data layer. These data elements are used throughout [!DNL Experience Platform Tags] in [!UICONTROL rules] and [!UICONTROL extensions].
1. In either the [!DNL Analytics] extension's global variables section or in a [!DNL Tags rule], assign the values in [!UICONTROL data elements] to [!UICONTROL props], [!UICONTROL eVars], [!UICONTROL pageName], and other [!DNL Analytics] variables.
1. Trigger a beacon that sends the data into [!DNL Analytics].

The following video walks you through the process.

>[!VIDEO](https://video.tv.adobe.com/v/25899/?quality=12&learn=on)

>[!NOTE]
>
>The specific data layer used in this video may not be considered "best practice" for your organization. The concept of using a data layer for surfacing important data to your digital marketing solutions is best practice.