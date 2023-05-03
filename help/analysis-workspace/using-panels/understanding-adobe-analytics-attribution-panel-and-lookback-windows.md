---
title: Understanding Adobe Analytics Attribution Panel & Lookback Windows
description: Learn how to use the Attribution Panel and Lookback Window to understand customer behavior and customize how dimension items get credit for success events.
feature: Attribution
role: User
level: Experienced
doc-type: Article
last-substantial-update: 2023-05-02
jira: KT-13181
thumbnail: KT-13181.jpeg
---

# Understanding Adobe Analytics Attribution Panel & Lookback Windows

Learn how to use the Attribution Panel and Lookback Window to understand customer behavior and customize how dimension items get credit for success events.

## Using the Attribution Panel

![Delorean](assets/delorean.png)

'Great Scott!'

As soon as I thought about the [Attribution Panel](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/panels/attribution.html) and **Lookback Window**, I was reminded of the song "Back in Time" by Huey Lewis and the News; then of course, I was also reminded that our typical response to many new tools like these is to just put off trying to use it, because they look so complicated.

I mean really, just look at all those options, switches, panels, readouts, and knobs.  And seriously, let's talk about that flux capacitor.  Wait, did I just say flux capacitor?

OK, I will admit the **Attribution Panel** is a fairly complex tool; however, our typical job as analysts, day in and day out, is to use a highly complex tool to look at what happened in the past.  That tool is called **Adobe Analytics**!

Therefore, why should we allow something like a little fear to stand in the way of such a cool and powerful tool that allows us to literally look         backward in time every day?

We're all about that stuff, right?  RIGHT???!!  (I mean, c'mon, I'm pretty sure it's still OK and "politically correct" to call us geeks?)

Ah, who cares?  Gear up, Geeks, Nerds, Goobers, Dweebs, and Techies (yes even the Trekkies), I can hear the car stereo now: 

 "So take me away, I don't mind!  But you better promise me… I'LL BE BACK IN TIME!"

I have your attention, now, right?  Great!


Let's break things down a little bit.  Now that we're all excited about **time travel**, let's take a step back and establish what the **Attribution Panel** really is:

![Time Control](assets/time-control.gif)

No, no, no, no, no!  Let's not get distracted just yet.  Maybe, let's try that again:

![Attribution Window](assets/attribution-window.png)

In **Attribution**, simply consider how events/actions might be caused by an individual, several individuals, or one or any number of different things over time.

According to [Adobe](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/component-settings/attribution.html), attribution gives analysts the ability to customize how dimension items get credit for success events.  In fact, no given customer journey is ever truly linear and is less often predictable.  Moreso, each customer will proceed at their own pace; often they might double back, stall, drop out, or engage in other non-linear behavior. These organic actions make it difficult or practically impossible to know the impact of marketing efforts across the customer journey. It also hampers efforts to tie multiple channels of data together.

Does any of this sound familiar to you?  Think about it in the context of Marty McFly's journey:

![Back to the Future 1](assets/back-to-the-future1.png)![Back to the Future 2](assets/back-to-the-future2.png)

From the point when he fled the Twin Pines Mall parking lot to when he literally threw himself out of the DeLorean before it was obliterated by a 210-ton locomotive seems far from linear, and it's nothing anyone could have predicted.

Yet, through the power of movie magic, we get to follow Marty's path through time and understand all of his touchpoints, his stalls, double-backs, and dropouts.

## Attribution Models

In real life, we get to use the **Attribution Panel** to see several different things.  For instance, the **Attribution Models** show us how our **conversions** are distributed across **hits** in any particular group.

Simply put, if 10 people press a button to step through a door, our Attribution Models are going to tell us which of those 10 people we want to give the credit for pressing that button.  With that in mind, here are some examples of how the attribution models might affect those 10 people:
*    **First Touch**: This one is exactly like it sounds.  In this case, it gives 100% credit to the first person who walked through the door.  For this, marketers are more likely to use this for tactics like Social or Display, but it is often a great tactic for on-site product recommendation effectiveness.
*    **Last Touch**: Also exactly like it sounds.   This model gives 100% credit to the last person who walked in the door.  This model is often used to analyze things like Search and short-term marketing cycle campaigns.
*    **Linear**: This gives equal credit to every single person who walked through the door.  That's right – You get a DeLorean, and you get a DeLorean, and you get a DeLorean.  EVERYBODY GETS A DELOREAN!!!
*    **U-Shaped**: This one gives 40% of the credit to the first one in the door, spreads 20% of the credit to everyone in between and then gives 40% to the last one through.  Think about a situation where you want to recognize the majority conversions on both the front and back end, but also want to sprinkle a small amount of the credit across some of the contributing interactions in between.
*    **Time Decay**: I would be remiss if I didn't share this one with you before I send you out to out to the official documentation to review the remaining models.  Like Doc Brown's plutonium, this model literally has a half-life that exponentially decays!  In this case, the default parameter for this model's half-life is 7 days.  The way it works is to then apply weight to each Marketing Channel, based on the amount of time that passes after the initial touchpoint and when the customer converts.

For additional information about this and the remaining **Attribution Models**, [click here](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/attribution/models.html).

To make this even more interesting, let's talk about the **Lookback Windows**.

Yup, here we go - take us BACK IN TIME!!  Because here's where the fun begins!

Adobe defines **Lookback Windows** as "the amount of time a conversion should look back to include touch points. Attribution models that give more credit to first interactions see larger differences when viewing different lookback windows."

*    **Visit lookback window**: Looks back up to the beginning of a visit when a conversion happened
*    **Visitor lookback window**: Looks at all visits back up to the 1st of the month of the current date range.
*    **Custom lookback window**: Allows you to expand the Attribution Window beyond the reporting date range up to a maximum of **90 days**.

If you've seen ALL of the Back to the Future movies, then you know Marty McFly went back in time more than once, and you also know he went back to 1955 more than once.  If we hinge upon the acquisition of "Gray's Sports Almanac" as our conversion event, then consider the following:

![Sports almanac](assets/sports-almanac.png)

1.    A little before **1:30am** on **October 26, 1985**, Marty McFly goes back in time to **November 5, 1955**, where he first runs over a pine tree in a time-traveling DeLorean.  Over the next week and a half, he interacts with multiple people, including his parents, ultimately affecting the future by influencing his dad to stand up to a bully named Biff, so his dad can realize his own potential to become a successful science-fiction author.
1.    Later the same morning on **October 26, 1985**, Doctor Emmett Brown arrives on Marty McFly's driveway to inform him and his girlfriend that something has gone horribly wrong with their kids and they must rush to the future to fix their problems.  As they leave, their departure is witnessed by Biff, who finds it odd to see a flying DeLorean.  Later, in the future, as Biff again witnesses a flying DeLorean and even later catches sight of "two versions" of Marty, he starts to put things together.   When he overhears Doc Brown and Marty arguing how the "time machine" should never be used for personal gain and only for research (because Marty had been mulling over taking a sports almanac back to the past to make some personal bets), Biff steals the time machine while the two are distracted to deliver the sports almanac to his younger self in the past.
1.    After their trip to the future, Doc Brown and Marty return to an **October 26, 1985** they don't recognize, and they deduce the timeline has been altered by an evil Biff.  Realizing they must fix what happened, Doc and Marty resolve to return to **November 12, 1955**, the fateful night when everything was changed by Marty when he first visited **1955**.  Doc and Marty ultimately save the day by stealing back the sports almanac that Old Biff from the future had delivered to Young Biff in **1955**, but not without another twist you really need to watch the full trilogy of movies to truly enjoy and understand.

Depending on our **Attribution Model** and **Lookback Window**, we can end up with some interesting scenarios:

*    Using **first touch** and a **visit lookback window**, attribution looks at Marty's visit where the most recent "conversion" happened, which is when he and Doc manage to steal the sports almanac back from Young Biff and maintain his aversion to manure. 

![Biff 1](assets/biff1.png)![Biff 2](assets/biff2.png)
  
*    Believe it or not, using **first touch** and a **visitor lookback window**, attribution would favor the conversion where Biff ultimately wins.
*    Applying a **linear lookback window** would result in a multi-verse where every timeline exists.  Sorry, this isn't **Marvel** or **Star Trek**!

And at this point, I hope you're starting to get the idea.

So, what does all this mean for us as analysts?

The **Attribution Panel** and **Lookback Window** give us the power to look beyond the simple, surface-level data and dive deeper into the customer journey. By understanding which touchpoints had the greatest impact on conversions, we can make informed decisions about our marketing strategies and allocate resources more effectively.

Remember, after you have your **Attribution Models** and **Lookback Windows** selected, you still have the ability to further manipulate your data by filtering it with a segment or any other component you wish.  Furthermore, after the Panel is rendered, you have all the functionality of a traditional **Workspace**, which means you're officially licensed to drive 88 mph!

## Finally Putting it Into Practice

Now that you've got the concepts down, imagine you're running a marketing campaign and trying to determine which channel is the most effective for driving conversions. With the help of the **Attribution Panel**, you can see not only the **Last Touch**, but also the **First Touch**, **Same Touch**, and any other model you choose, to determine which channels are the most effective in driving your conversions. Then, this information can be used to optimize your campaigns and improve overall performance.

Now that you've seen what it can do, don't be intimidated by the seemingly complex features of the **Attribution Panel**.  **Face** it.  **Embrace** it.  **Understand** it.  Most of all, use it to your advantage. The **Attribution Panel** and **Lookback Window** are the keys to unlocking a deeper understanding of your customers and their journey with your brand.

Now, we can travel "back in time" with confidence and use the power of our trusty time machine (aka,  **Adobe Analytics**) to make data-driven decisions; and, most importantly, remember, "Where we're going, we don't need roads!" (Just a flux capacitor, and a keen eye for attribution!)
 
![Back to the future](assets/back-to-the-future3.png)

## Author

This document was written by:

![Jeff Bloomer](assets/jeff-headshot.png)

**Jeff Bloomer**, Manager, Digital Analytics at Kroger Personal Finance

Adobe Analytics Champion
