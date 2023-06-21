---
title: Understanding Adobe Analytics attribution panel and lookback windows
description: Learn how to use the attribution panel and lookback window to understand customer behavior and customize how dimension items get credit for success events.
feature: Attribution
role: User
level: Experienced
doc-type: Article
last-substantial-update: 2023-06-20
jira: KT-13181
thumbnail: KT-13181.jpeg
---

# Understanding Adobe Analytics attribution panel and lookback windows

When I first thought about the [attribution panel](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/panels/attribution.html?lang=en) and **lookback window**, I was immediately reminded of the concept of '*time travel'*; then, of course, I was also reminded our typical response to many new tools like these is to simply put off trying to use it, because they look so complicated.

I mean honestly, just look at all those options, switches, panels, readouts, and knobs.  And seriously, let's talk about those complicated flashing lights, hoses, gauges…. WAIT!!  This is not the time to get distracted talking about time machines, we just don't have the time… or do we?

I will admit the **attribution panel** is a fairly complex tool; however, our typical job as analysts, day in and day out, is to use another one of our favorite and highly complex tools to also take a look at what happened in the past. That tool is called ***Adobe Analytics***!  So yes, to answer our very relevant question, I believe these two things say we have plenty of time.

Therefore, why should we allow something like a little fear to stand in the way of such amazing, sophisticated, and powerful tools like these that literally allow us to look *backward* in time, each and every single day?

After all - this is TIME TRAVEL, folks!!  We're all about that kind of stuff.  Right???!!

So, what are we waiting for - a shiny metal car, a police box, or a vintage telephone booth using the wiring of an old umbrella as its antenna to show up on our doorstep?

No!  We've got something even better, so let's strap in and hang on!

Well… you get the idea.


Now that we're all excited about time travel, let's take a deep breath, step back a little, establish what the **attribution panel** *really* is, and break things down a little bit:

![Attribution](assets/attribution.png)

*Figure 1 - Numbers displayed inline with text further below*

In **attribution**, simply consider how events/actions might be caused by an individual, several individuals, or one of any number of different events over time.

According to [Adobe](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/attribution/overview.html?lang=en), *attribution* gives analysts the ability to customize how *Dimension* items receive credit for *success events*.


**⛔** DETOUR: Just a quick note to call out that **attribution models** are so frequently associated with **marketing channels** that I purposely *crossed out* CHANNEL in the image above to illustrate it is possible to perform **attribution** analysis against most any other ***dimension***.


In fact, rarely is any given customer journey truly linear and even less often predictable.  More so, each customer will proceed at their own pace; often, they might double back, stall, drop out, or engage in other non-linear behavior. These organic actions make it difficult or practically impossible to know the impact of marketing efforts across the customer journey. It also hampers efforts to tie multiple channels of data together.

That's right.  Leave your "domino" analogies at the doorway and open your minds to concepts more along the lines of the butterfly effect and string theory - but like everything else, we need to start with some of the basics.

## **Attribution models**

When we use the **attribution panel**, we may begin to observe several different things.  For instance, the **attribution models** demonstrate to us how our *conversions* (i.e., ***success metrics***) may be distributed across *hits* in any given group.

Simply put, if **10 people** press a **BIG RED BUTTON** to step through a door, our **attribution models** are going to tell us which of those **10 people** we want to assign "credit" - or even better said, how *much* "credit" we want to assign them - for pressing said button.

![Button](assets/button.png)

Keeping this in mind, here are a few examples of how the **attribution models** might affect those **10 people**:

- **First touch**: This model works exactly like it sounds by giving **100% credit** to the *first* person who walked through the door.  Marketers are more likely to use this approach for tactics like ***social media*** or ***display***; however, it is also a great tactic to often use for on-site product recommendation effectiveness.
- **Last touch**: This tactic also works exactly like it sounds, but instead gives **100% credit** to the LAST person who walked through the door.  This model is typically used to analyze things like ***natural (organic) search*** and other *short-term* marketing cycle campaigns.
- **Linear**: This model distributes equal credit across EVERY SINGLE PERSON who walked through the door.

Caution is recommended here, though, because you have the potential to spread your results very thin very quickly when applying this tactic, considering the longer it runs and the larger the audience it hits.

- **U-Shaped**: This approach assigns **40%** of the credit to the *first person* in the door, spreads **20%** of the credit across *everyone in between*, and then gives **40%** to the **last one** through. This model will most often be used in situations when you have a **long conversion/sales cycle** containing *several touchpoints* along the way.  In this case, your goal is to primarily highlight the ***first*** and ***last*** marketing tactics that contributed to the customer converting.
- **J**-**Shaped** and **Inverse J**:
  - Think about **U-Shaped**, but instead this model assigns **60%** credit to the *last person* walking through the door, **20%** to the *first*, and then *divides* the remaining **20%** across *everyone else* in the middle.  **Inverse J** does the exact opposite.

The goal here is to put most of your emphasis, either at the *beginning* or the *end* of your campaign; however, you still want to assign a certain amount of credit to the contributing item on the opposite end while acknowledging the "little guys" along the way. 

- **Time decay**: Now, I would be remiss if I didn't share this one. This model literally has a half-life that exponentially decays - over time!  In this case, the *default* parameter for this model's half-life is **7 days**.  The way it works is to then apply *weight* to each **marketing channel**, *based on the amount of time* that passes after the *initial touchpoint* and when the customer converts.

  **Time decay** and **U-shaped attribution models** are both typically used to measure longer-termed campaigns, but as you can see, they have slightly different goals, based on how they ultimately *weigh* the value of the outcome.

- **Custom**: You pick and choose who's going to get credit.  It's your campaign!

For additional information about these and other attribution models, [click here](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/attribution/models.html?lang=en)

To make this even more interesting, let's talk about turning back the clock!

## **Lookback windows**

Now it's time to start taking your mind to the next level.  This is where we literally add the time travel element to our analysis - and again, we are beginning with the basics.

***Adobe*** defines **lookback windows** as "the amount of time a conversion should look back to include touch points. Attribution models that give more credit to first interactions see larger differences when viewing different lookback windows."


In other words, **lookback windows** determine the time period during which *conversions* are considered and provide *context* to the attribution analysis. ***Adobe Analytics*** offers three types of **lookback windows**:

- **Visit lookback window:** Looks back to the beginning of a ***visit*** when a conversion happened, providing insights into the immediate interactions leading up to conversions.

  Remember this is typically the shortest **lookback window** to use.
- **Visitor lookback window:** Looks at all ***visits*** back up to the first of the month within the selected **date range**, offering a much broader view of the customer's interactions and helps identify patterns over time.
- **Custom lookback window:** Allows you to expand the **attribution window** beyond the reporting **date range** up to a *maximum* of **90 days**.  It provides *flexibility* in capturing touchpoints that occurred *outside* the selected **date range**, ensuring a comprehensive analysis.

By adjusting a given **lookback window**, analysts may then examine the impact of one or more touchpoints within specific time frames and gain greater insights into how different durations affect attribution results.

## **Bringing it all together**

So, what does all this mean to us as analysts?

The **attribution panel** and **lookback window** give us the power to look beyond the mundane, surface-level data, and dive deeper into the customer journey. By understanding which touchpoints had the greatest impact on *conversions*, we can make informed decisions about our marketing strategies and allocate resources more effectively.

Remember, after you have your **attribution models** and **lookback windows** selected, you may still further manipulate your data by filtering it with a  **segment,** or any other component you wish at this point.  Furthermore, after the panel is rendered, you have all the functionality of a traditional Workspace at your disposal.

## **Finally putting it into practice**

Now that you've got the concepts down, imagine you're running a marketing campaign and trying to determine which channel is the *most effective* for driving conversions. With the help of the **attribution panel**, not only can you see the **last touch**, but also the **first touch**, **same touch**, and any other **model** you choose to determine which **channels** are the *most effective* in driving your *conversions*. Then, this information can be used to *optimize* your campaigns and improve overall performance simply by turning back the clock with the **lookback window** of your choice!

Now that you've seen what it can do, don't be fooled or intimidated by the seemingly complex features of the attribution panel.  **Face it**.  *Embrace* it.  Understand it*.*
BUT MOST OF ALL - *Use it to your advantage.* The **attribution panel** and **lookback window** are the keys to unlocking a deeper understanding of your customers and their journey with your brand.

Now, we can travel "[back in time](https://youtu.be/gVryJmZNFdU)" with confidence and use the power of our trusty time machine (a.k.a., ***Adobe Analytics***) to make data-driven decisions.
