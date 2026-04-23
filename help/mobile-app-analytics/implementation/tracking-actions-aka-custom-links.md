---
title: Tracking Actions (AKA Custom Links) in a Mobile App with the Experience Platform SDK
description: Actions are events that occur in your mobile app. In this video, learn how to use the trackAction API to track and measure an action.
feature: Mobile SDK
topics: null
activity: implement
doc-type: technical video
team: Technical Marketing
kt: 2563
topic: Mobile
role: Developer
level: Experienced
exl-id: 541c51b8-638e-43b4-90ac-0ce94290a141
TQID: https://experienceleague.adobe.com/msvft7mQiNGjLqGEezPIbwruvSbsunPGUIFF1q7vlT0
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
    internal-label: Metrics
  - id: fd307ce7-56f5-4ee3-af68-a7833ff6e85e
    internal-label: API
subfeature_v2:
  - id: f1f1a2d4-0976-4881-b091-c2bb8de7ffac
    internal-label: Events
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
---
# Tracking Actions (AKA Custom Links) in a Mobile App with the Experience Platform SDK {#tracking-actions-aka-custom-links-in-a-mobile-app-with-the-experience-platform-sdk}

Actions are events that occur in your mobile app. In this video, learn how to use the trackAction API to track and measure an action.

>[!VIDEO](https://video.tv.adobe.com/v/26268/?quality=12&learn=on)

This is the API that you should use to track all non-screen-load actions on your site. If the screen is coming up, then use trackState, which triggers a page view hit. Otherwise, use trackAction to send in variables associated with the action that is taking place.

This data comes in as `contextData`, which also means that you will then need to use [!UICONTROL Processing Rules] to take the mobile data from those `contextData` variables and map it into [!DNL eVars], [!DNL Props], Events, etc. in Adobe Analytics.

For more information about trackAction, please see the [documentation](https://developer.adobe.com/client-sdks/documentation/getting-started/track-events/#track-user-actions-for-adobe-analytics).
