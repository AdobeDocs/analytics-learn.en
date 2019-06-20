---
title: Using best practices when tracking SPA in Adobe Analytics
seo-title: Using best practices when tracking SPA in Adobe Analytics
description: In this document, we will describe several best practices that you should follow and be aware of as you are using Adobe Analytics to track Single Page Applications (SPA). This doc will focus on using Launch by Adobe, which is the recommended implementation method.
seo-description: In this document, we will describe several best practices that you should follow and be aware of as you are using Adobe Analytics to track Single Page Applications (SPA). This doc will focus on using Launch by Adobe, which is the recommended implementation method. Adobe Analytics
uuid: 13658531-432b-49ae-848a-33ddee8a83c4
products: SG_ANALYTICS
discoiquuid: b25e715a-b820-4d66-a5c4-47a74f1fd446
feature: implementation - spa pages
topics: spa
audience: implementer
activity: implement
doc-type: technical video
author: Doug Moore
team: Technical Marketing
kt: 1389
---

# Using best practices when tracking SPA in Adobe Analytics {#using-best-practices-when-tracking-spa-in-adobe-analytics}

In this document, we will describe several best practices that you should follow and be aware of as you are using Adobe Analytics to track Single Page Applications (SPA). This doc will focus on using Launch by Adobe, which is the recommended implementation method.

INITIAL NOTES:

* The items below are going to assume that you are using Launch by Adobe to implement on your site. The considerations would still exist if you are not using Launch, but you would need to adapt them to your implementation method.
* All SPAs are different, so you may need to tweak some of the following items to best meet your need, but we wanted to share some best practices with you; things that you need to think about as you are implementing Adobe Analytics on SPA pages.

## Simple diagram of working with SPAs in Launch by Adobe {#simple-diagram-of-working-with-spas-in-launch-by-adobe}

![spa for analytics in launch](assets/spa_for_analyticsinlaunch.png)

**NOTE:** As stated, this is a simplified diagram of how SPA pages are handled in an Adobe Analytics implementation using Launch by Adobe. In the following sections of this page, we will discuss the steps and any issues that you should carefully consider or act on.

## Setting the data layer {#setting-the-data-layer}

When new content is loaded on a SPA page, or when an action takes place on a SPA page, one of the first things you should do is to update the data layer. This needs to happen BEFORE the custom event fires and triggers rules in Launch, so that Launch can pick up the new values from the data layer and push them into Adobe Analytics.

Following is a sample data layer, the elements of which could be changed on view change or action on your SPA. For example, on a full/majority screen change, it would be common to change a “pageName” element, so that the new one could be captured in Launch and sent into Adobe Analytics.

```JavaScript
<script>
    digitalData = {
        pageInstanceID: "Launch by Adobe Demo Site",
        page:{
            pageInfo:{
                pageID: '2745374',
                pageName: 'acs demo - product listing page'
            },
            attributes:{
                project: "Adobe Launch Project"
            }
        },
        user : [ {
          "profile" : [ {
            "attributes" : {
              "gender" : "male",
              "age" : "35"
            }
          } ]
        }],
        libraries : {
          adobe : {
            launch : {
              state : 0, // 0 = not loaded , 1 = loaded
              domain : "assets.adobedtm.com"
            }
          }
        }

     };
    </script>

```

## Setting Custom Events and Listening in Launch by Adobe {#setting-custom-events-and-listening-in-launch-by-adobe}

When new content loads on the page, or when an action happens on the site, you will want to inform Launch so that it can run a rule and send data to Analytics. There are a couple different ways to do this: Direct Call rules or Custom Events.

* Direct Call Rules: in Launch, you can set up a direct call rule that executes when it is called directly from the page. If your page load or your action on your site is very simple, or if it is unique and can execute a specific set of instructions every time (set eVar4 to X and trigger event2 every time), then you can use a direct call rule. See Launch documentation regarding creating direct call rules.
* Custom Events: For more functionality, and for the ability to dynamically attach a payload with different values, you should set custom JavaScript events and listen for them in Launch, where you can use the payload to set variables and send the data into Adobe Analytics. It is more likely that you will need this functionality, and so this option is considered the best practice. However, each function on your site can determine which method will be most appropriate. We will move forward in this document assuming that you will need to use this custom events method.

**Examples:** In [THIS](https://helpx.adobe.com/experience-manager/kt/integration/using/launch-reference-architecture-SPA-tutorial-implement.html) help document, there are links to sample SPA sites that have implemented Analytics (and other Experience Cloud solutions), as well as documents describing what has been implemented. In these SPA examples, the following custom events have been used:

* event-view-start: This event should fire on the view start of the view/state that is loading.
* event-view-end: This event should be fired even when a view/state change has occurred and all SPA components on the page have finished loading. This is the event that typically triggers a call into Adobe Analytics.
* event-action-trigger: This event should fire when any event occurs on the page except view/state load. This could be a click event or a smaller content change without a view change.

Please see the above-referenced pages/docs for more information about how/when they are fired. You don’t have to use these same event names, but the functionality listed here is recommended best practices. The following video will show a sample site and where in Launch to listen for the custom events.

>[!VIDEO](https://video.tv.adobe.com/v/23024/?quality=12)

## Running s.t() or s.tl() in the Launch Rule {#running-s-t-or-s-tl-in-the-launch-rule}

One of the most important things to understand for Analytics when working with a SPA is the difference between s.t() and s.tl(). You will be triggering one of these methods in Launch to send data into Analytics, but you need to know when to send each one.

* **s.t()** - The “t” stands for “track” and is a normal page view. Even though the URL may not change, does the view change enough that you would *consider* it a new “page”? If so, set the s.pageName variable and use s.t() to send the call into Analytics

* **s.tl()** - The “tl” stands for “track link” and is normally used for tracking clicks or small content changes on the page, as opposed to a full screen change. If the change on your page is small, so that you wouldn’t consider it a full new “page”, use s.tl() and do not worry about setting the s.pageName variable, as Analytics will ignore it.

**TIP:** Some people use a general guideline that if the screen changes more than 50%, it should be considered a page view and use s.t(). If it is less than 50% change to the screen, use s.tl(). However, it is totally up to you and what you consider a new “page” and how you would like to track your site in Adobe Analytics.

The following video shows where/how to trigger s.t() or s.tl() in Launch by Adobe.

>[!VIDEO](https://video.tv.adobe.com/v/23048/?quality=12)

## Clearing Variables {#clearing-variables}

When tracking your site with Adobe Analytics, you of course only want to send the right data into Analytics at the right time. In a SPA environment, a value tracked in an Analytics variable can persist and be re-sent into Analytics, potentially when we no longer want it to. For this reason, there is a function in the Analytics Launch extension to clear the variables, so that you have a fresh slate when you run the next image request and send data into Analytics.

In the diagram above, we have it listed at the end of the process, clearing the variables *after* you send in the hit. In reality, it can be done either before OR after the hit gets sent in, but should be consistent in your Launch rules, so that you always clear either before or after setting variables and sending them in. Remember, if you are going to clear the variables *before* you run s.t(), make sure that you clear the variables first, then set the new variables, and then finally send the new stuff into Analytics (was that too obvious? Haha).

**NOTE:** Clearing variables is not always needed when running s.tl(), because s.tl() requires the usage of the linkTrackVars variable alongside it each time to tell Analytics which variables are going to be set (automatically added behind the scenes in Launch). This means that errant variables don’t usually come in when using s.tl(), but it is very much recommended when using s.t() in a SPA environment. All that being said, I would like to recommend it as a best practice to use the Clear Variables function for both s.t() and s.tl() in a SPA environment, just to ensure quality data collection.

The following video shows where/how to clear the variables in Launch by Adobe.

>[!VIDEO](https://video.tv.adobe.com/v/23049/?quality=12)

## Additional Considerations {#additional-considerations}

### Custom Code Windows in Launch {#custom-code-windows-in-launch}

In the Launch Analytics extension, there are two places where you can insert custom code: The library management section and the extra “Configure Tracker Using Custom Code” section.

![Launch Analytics custom code windows](assets/launch_analyticscustomcodewindows.png)

It is important to know that either one of these locations are really only going to run the code in them once, when the initial page load happens on your SPA page. If you need the code to run on a view change or on an action on your site, you should add an additional Action to the appropriate **rule** (E.g. in the “page load: event-view-end” rule), so that the code executes every time that rule runs. When creating that Action in the rule, set *Extension = Core* and *Action Type = Custom Code*.

### “Hybrid” SPA/Regular Sites {#hybrid-spa-regular-sites}

Some sites are a combination of “regular” pages and SPA pages. In this instance, you will need to use a strategy that works for both page types. When configuring your custom events on the site, and triggering the rules in Launch, be careful that there aren’t double hits going into Analytics from the page, based on hash changes, etc. (if that is how you have chosen to trigger the Launch rule). In this case, you will need to suppress one of the page views so that it doesn’t give you faulty data in Adobe Analytics.

If you decide to break the functionality out into separate rules so that you have more control over it, be sure to remember/document that you have done this, so that that any changes to one rule can be made to the other rule as well, protecting your Analytics data integrity.

### Integration with Target via A4T {#integration-with-target-via-a4t}

Just a quick callout here. If you are integrating with Target using A4T, make sure that the Target request and the Analytics request on the same view change have the same SDID. This will ensure that your data properly synchronizes on the solutions.

To see the hits, use a debugger or packet sniffer program. You can also use the newly released Experience Cloud Debugger, a Chrome extension that can be downloaded [HERE](https://chrome.google.com/webstore/detail/adobe-experience-cloud-de/ocdmogmohccmeicdhlhhgepeaijenapj). Target should be firing first on the page, so you can also check that in the JavaScript console or debugger.

## Additional Resources {#additional-resources}

* [SPA discussion on the Adobe forums](https://forums.adobe.com/thread/2451022)
* [Reference Architecture sites to show how to implement SPA in Launch by Adobe](https://helpx.adobe.com/experience-manager/kt/integration/using/launch-reference-architecture-SPA-tutorial-implement.html)