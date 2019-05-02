---
title: Using Report Builder to Build Adobe Analytics 1.4 API Requests
seo-title: Using Report Builder to Build Adobe Analytics 1.4 API Requests
description: In this video, we will walk through how to take debug Report Builder requests and use them to learn how to craft your own Analytics API queries.
seo-description: In this video, we will walk through how to take debug Report Builder requests and use them to learn how to craft your own Analytics API queries.
uuid: 08e4b4f4-5e8e-4ae9-bf77-8edb33671e21
products: SG_ANALYTICS
discoiquuid: 73a079bc-cef8-46ae-af1d-081398b2c29c
targetaudience: target-audience new;target-audience ongoing
index: y
internal: n
snippet: y
---

# Using Report Builder to Build Adobe Analytics 1.4 API Requests{#using-report-builder-to-build-adobe-analytics-api-requests}

>[!VIDEO](https://video.tv.adobe.com/v/25442/?quality=12)

**UPDATE**: Report Builder updated how it requests the data slightly. You can still use the approach from this video, but the information will be slightly different in a debugger.

In a debugger:

1 - Search for api5.omniture.com. The number might vary from 1-5 depending on your data center.

2 - Go to the Request tab

3 - Search for 'Report.Queue' in the request.

There is also an alternate method to debugging requests like this, and it works just as well. You can turn on Report Builder logging from the Options mene and that will record the same information as a debugger would. Logs can be found under Documents/ReportBuilderLogs, and will be organized by day. You can search the file for 'Report.Queue' to find each of your requests. Logs also help with troubleshooting any issues.

For more information on this feature, visit [the documentation](https://www.adobe.io/).
