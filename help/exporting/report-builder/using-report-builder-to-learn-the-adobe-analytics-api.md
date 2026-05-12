---
title: Using Report Builder to learn the Adobe Analytics API
description: Report Builder is something we all know & love. So what if I told you that you could use what you know about Report Builder to advance your Adobe Analytics skillset even further? In this video, we will walk through how to take debug Report Builder requests and use them to learn how to craft your own Analytics API queries.
feature: Report Builder
topics: null
activity: use
doc-type: feature video
team: Technical Marketing
kt: 2345
role: User
level: Intermediate
exl-id: 8b8e0dac-2498-4fba-ba4b-585b309ae1fd
TQID: https://experienceleague.adobe.com/CnzT7nd58cibYkdt7hfAwgMF4kJR3clcTZYbditrsaM
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
    internal-label: Reports
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
    internal-label: Metrics
  - id: fd307ce7-56f5-4ee3-af68-a7833ff6e85e
    internal-label: API
subfeature_v2:
  - id: ac8a38fa-dec3-4581-8f64-178fde9f64e8
    internal-label: Report Builder
  - id: f836f655-eebe-4b76-82bc-697955ec1ce3
    internal-label: Calculated Metrics
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
---
# Using [!UICONTROL Report Builder] to learn the Adobe Analytics API {#using-report-builder-to-learn-the-adobe-analytics-api}

[!UICONTROL Report Builder] is something we all know & love. So what if I told you that you could use what you know about [!UICONTROL Report Builder] to advance your Adobe Analytics skillset even further? In this video, we will walk through how to take debug [!UICONTROL Report Builder] requests and use them to learn how to craft your own [!DNL Analytics] API queries.

>[!VIDEO](https://video.tv.adobe.com/v/25442/?quality=12&learn=on)

**UPDATE**: [!UICONTROL Report Builder] updated how it requests the data slightly. You can still use the approach from this video, but the information will be slightly different in a debugger.

In a debugger:

1 - Search for api5.omniture.com. The number might vary from 1-5 depending on your data center.

2 - Go to the [!UICONTROL Request] tab

3 - Search for '[!DNL Report.Queue]' in the request.

There is also an alternate method to debugging requests like this, and it works just as well. You can turn on [!UICONTROL Report Builder] logging from the [!UICONTROL Options] menu and that will record the same information as a debugger would. Logs can be found under [!UICONTROL Documents] > [!UICONTROL ReportBuilderLogs], and will be organized by day. You can search the file for 'Report.Queue' to find each of your requests. Logs also help with troubleshooting any issues.

For more information on this feature, visit the [documentation](https://www.adobe.io/).
