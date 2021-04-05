---
title: Using Report Builder to learn the Adobe Analytics API
description: Report Builder is something we all know & love. So what if I told you that you could use what you know about Report Builder to advance your Adobe Analytics skillset even further? In this video, we will walk through how to take debug Report Builder requests and use them to learn how to craft your own Analytics API queries.
feature: Report Builder
topics: 
activity: use
doc-type: feature video
team: Technical Marketing
kt: 2345
role: Business Practitioner
level: Intermediate
exl-id: 8b8e0dac-2498-4fba-ba4b-585b309ae1fd,9f472016-f994-4914-8278-b9f60ed8e503,9f472016-f994-4914-8278-b9f60ed8e503,8b8e0dac-2498-4fba-ba4b-585b309ae1fd
---
# Using [!UICONTROL Report Builder] to learn the Adobe Analytics API {#using-report-builder-to-learn-the-adobe-analytics-api}

[!UICONTROL Report Builder] is something we all know & love. So what if I told you that you could use what you know about [!UICONTROL Report Builder] to advance your Adobe Analytics skillset even further? In this video, we will walk through how to take debug [!UICONTROL Report Builder] requests and use them to learn how to craft your own [!DNL Analytics] API queries.

>[!VIDEO](https://video.tv.adobe.com/v/25442/?quality=12)

**UPDATE**: [!UICONTROL Report Builder] updated how it requests the data slightly. You can still use the approach from this video, but the information will be slightly different in a debugger.

In a debugger:

1 - Search for api5.omniture.com. The number might vary from 1-5 depending on your data center.

2 - Go to the [!UICONTROL Request] tab

3 - Search for '[!DNL Report.Queue]' in the request.

There is also an alternate method to debugging requests like this, and it works just as well. You can turn on [!UICONTROL Report Builder] logging from the [!UICONTROL Options] menu and that will record the same information as a debugger would. Logs can be found under [!UICONTROL Documents] > [!UICONTROL ReportBuilderLogs], and will be organized by day. You can search the file for 'Report.Queue' to find each of your requests. Logs also help with troubleshooting any issues.

For more information on this feature, visit the [documentation](https://www.adobe.io/).
