---
title: Tracking Actions (AKA Custom Links) in a Mobile App with the Experience Platform SDK
description: Actions are events that occur in your mobile app. In this video, learn how to use the trackAction API to track and measure an action. 
feature: implementing mobile analytics
topics: 
audience: administrator
activity: implement
doc-type: technical video
team: Technical Marketing
kt: 2563
---

# Tracking Actions (AKA Custom Links) in a Mobile App with the Experience Platform SDK {#tracking-actions-aka-custom-links-in-a-mobile-app-with-the-experience-platform-sdk}

Actions are events that occur in your mobile app. In this video, learn how to use the trackAction API to track and measure an action.

>[!VIDEO](https://video.tv.adobe.com/v/26268/?quality=12)

This is the API that you should use to track all non-screen-load actions on your site. If the screen is coming up, then use trackState, which triggers a page view hit. Otherwise, use trackAction to send in variables associated with the action that is taking place.

This data comes in as [!DNL contextData], which also means that you will then need to use [!UICONTROL Processing Rules] to take the mobile data from those [!DNL contextData] variables and map it into [!DNL eVars], [!DNL Props], Events, etc. in Adobe Analytics.

For more information about trackAction, please see the [documentation](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/mobile-core/configuration-reference/mobile-core-api-reference).
