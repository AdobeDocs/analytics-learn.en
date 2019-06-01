---
title: Tracking Actions (AKA Custom Links) in a Mobile App with the Experience Platform SDK
seo-title: Tracking Actions (AKA Custom Links) in a Mobile App with the Experience Platform SDK
description: Actions are events that occur in your mobile app. In this video, learn how to use the trackAction API to track and measure an action. 
seo-description: Actions are events that occur in your mobile app. In this video, learn how to use the trackAction API to track and measure an action. 
uuid: 0386ff9e-18f6-4487-937e-79ff193bcd4a
products: SG_ANALYTICS
products: SG_MOBILEAPPS
discoiquuid: 7ac9cd8b-8dc3-4d53-9964-63b5aea47796
targetaudience: target-audience new;target-audience ongoing
index: y
internal: n
snippet: y
---

# Tracking Actions (AKA Custom Links) in a Mobile App with the Experience Platform SDK {#tracking-actions-aka-custom-links-in-a-mobile-app-with-the-experience-platform-sdk}

Actions are events that occur in your mobile app. In this video, learn how to use the trackAction API to track and measure an action.

>[!VIDEO](https://video.tv.adobe.com/v/26268/?quality=12)

This is the API that you should use to track all non-screen-load actions on your site. If the screen is coming up, then use trackState, which triggers a page view hit. Otherwise, use trackAction to send in variables associated with the action that is taking place.

This data comes in as contextData, which also means that you will then need to use Processing Rules to take the mobile data from those contextData variables and map it into eVars, Props, Events, etc. in Adobe Analytics.

For more information about trackAction, please see the [documentation](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/mobile-core/configuration-reference/mobile-core-api-reference).
