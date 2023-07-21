---
title: Building customer journey segments - part two 
description: In part two, learn how to build purchase and retention visit intent segments to understand customers' buying journey and personalize content. Using signals like "Book Now" clicks or logins, we identify purchase and retention intent for effective analysis and targeted marketing.
feature: Segmentation
role: User
level: Experienced
last-substantial-update: 2023-07-21
jira: KT-13476
thumbnail: KT-13476.jpeg
---

# Building customer journey segments - part two

In part two, learn how to build purchase and retention visit intent segments to understand customers' buying journey and personalize content. Using signals like "Book Now" clicks or logins, we identify purchase and retention intent for effective analysis and targeted marketing.

## Building Purchase and Retention Visit Intent Segments

In our last post, we described the process of creating visit intent segments, and built our first visit intent segment, One Hit Wonders. Today we'll build our Purchase and Retention segments. We had segmented about 23% of our visits, and we built our placeholders for the remaining Visit Intent segments.

![Image 1](assets/image-1.png)

The visit intent segments we are building now are the foundation of building visitor-based customer journey segments. We will build those visitor-based journey segments after we've built our visit intent segments.

Recall that building visit intent segments is a process of elimination. So, we aren't building these segments in chronological order. We are building our visit intent segments in order of easiest to define to tougher to define:

1. Intent: 0 - One Hit Wonders
1. Intent: 3 - Purchase
1. Intent: 4 - Retention
1. Intent: 2 - Consideration
1. Intent: 1 - Awareness

In our last post, I called the "Purchase" segment "Booking" since I'm in the travel business. But going forward we'll call it the Purchase segment to make it easier to apply to multiple industries.

The clearer the signal, the easier it is to build the segment. In our last post, we built our One Hit Wonders segment, which was the easiest to define since it's just bounced traffic. You'll find that the Purchase and Retention intent segments are also very easy to define, since they are based on very clear signals.

## Customer Journey is Different than Propensity to Purchase

As we look at building our Purchase Intent segment, it's important to remember that identifying where a customer is in their journey is different from propensity. You might have some purchase propensity models that score web visitors to predict how likely they are to make a purchase. These models are super useful, but they are different than the Purchase Intent segment we'll build today.

While a propensity model seeks to predict whether a visitor will purchase, our Visit Intent segments seek to understand where a person is in their buying journey. Using Intent segments to understand a customer's state of mind helps us to personalize content and tailor marketing to drive the right traffic to fuel our sales pipeline. So, our Purchase Intent segment looks for explicit behavioral signals that indicate a visitor is looking to make a purchase.

## Building the Purchase Visit Intent Segment

The Purchase Visit Intent segment is easy to define. In my case, anybody who clicks the "Book Now" button is indicating some sort of intent to book a cruise. That's similar to clicking "Checkout" for an online retailer, or a "Subscribe" link in a media context.

You'll need to exercise some judgment when deciding what signal to use for inferring purchase intent. We want our Purchase Intent segment to contain all purchases, but the conversion rate should not be 100%. So, we don't want to use the Purchase Confirmation or Thank You page for this segment.

Similarly, the Review Your Purchase page (or whatever is immediately before purchase confirmation) is likely too far down funnel to be useful for analysis and targeting.

As you go further up the funnel, it can become less clear whether or not the signal is useful for indicating that a customer intends to make a purchase. In my case, "Book Now" is similar to a retail "Checkout" link, and that's the signal I used. But in a retail context, Checkout may still be too far down the funnel and View Cart or even Add to Cart might be better. 

We can think of this as something like a grocery store. If somebody picks up a product off the shelf that doesn't mean they intend to buy it. Even if they put it in their cart, they might immediately put it back on the shelf. But if they put the product in their cart and start walking around with it, there's a pretty good chance that they mean to buy it. And if they get in the checkout line with that product it's a pretty good bet that they will buy.

I suggest using pages visited or other explicit purchase intent signals and avoiding other, less direct signals to identify purchase intent. For example, I would not use number of sessions or number of pages in a session or similar. These indirect signals indicate Consideration, not Purchase intent. Remember, the purpose of this segment is to infer the visitor's intent for the visit, not their propensity.

### Using Analytics Workspace to Identify Purchase Intent Signals

The Fallout report is very useful for identifying a good signal that indicates purchase intent. Look for a place that logically indicates intent. You can confirm that the step indicates intent when you see a notable fallout going to that step, often followed by a smaller fallout for the step immediately after.

![Image 2](assets/image-2.png)

It's also useful to look at conversion rates associated with the various pages on your site. This is especially helpful for identifying pages that indicate purchase intent but may not be required to make a purchase (such as financing pages, purchase configuration pages, etc.).

![Image 3](assets/image-3.png)

Finally, it's important to include all of the pages between purchase start and purchase confirmation in your segment. Visitors can bounce around and re-enter your purchase flow at different points.

### Excluding Other Segments

Recall from our first post that our Visit Intent segments need to be mutually exclusive and completely exhaustive. This is refrain you'll hear a lot in this series.

Be sure that your Purchase Intent segment excludes the One and Done segment. You should only need to exclude the One and Done segment because the signals we use for Purchase Intent are very specific.

Note that excluding the One and Done segment might exclude somebody who re-enters your site on a checkout page. This is OK. The very definition of One and Done is one page view, which means that even if a visitor enters or refreshes on a checkout page, their visit did not progress, therefore there's no expression of purchase intent.

### The Purchase Intent Segment in Segment Builder

The segment definition for Purchase Intent is very simple.

Using the visit container, include those pages or other actions that explicitly indicate an intent to make a purchase. If you have multiple include conditions, be sure to put them in a container joined by the "And" condition.

Add an Exclude container to the segment joined by the "And" condition. Add your One Hit Wonders segment definition (Page Views equals 1) to the Exclude container.

![Image 4](assets/image-4.png)

As best practice, be sure that you label your containers. You'll be glad you did, especially as our segment definitions become more complex.

Now that we've built the Purchase Intent segment, we can use the Visit Intent Data Quality Workspace to see that our Purchase Intent segment is mutually exclusive with our One and Done segment.

![Image 5](assets/image-5.png)

## Building the Retention Visit Intent Segment

In the cruise business, many guests come to our website to manage a booking but not necessarily to make a purchase. They can come to the site to enter travel information, review their itinerary, make dinner reservations, or a number of other things, without shopping for a cruise. Our guests can also purchase shore excursions or other enhancements to their experience. We consider these enhancements to be part of retention, so we keep them separate from our Booking segment (which we're calling "Purchase" in this blog series).

Retail customers might be able to make returns or manage their loyalty program. Media or Technology subscribers might be using the product. If your guest is on your website to manage their relationship with you, that's a Retention Visit and we should look at those signals. And if you provide an online product, like Media, Tech, Online Banking, or others, there are likely many other kinds of visit intent segments that we won't discuss in this series.

As with the Purchase Intent segment, we're looking for very explicit indications of intent. For me, we have an entire section of the site dedicated to managing a cruise so it's easy to identify those pages. This might be more complex for other businesses. Look for signals like logins, account management, visits to support pages, and similar.

I should note that "Retention" is a bit of an awkward name for this visit intent, since the visitor isn't on our site, "so I can be retained as a customer." Retention is our intention for that visit. Just remember to be empathetic to our customers and maintain a customer-first focus!

### Using Analytics Workspace to Identify Retention Intent Signals

Again, Analytics Workspace helps us identify Retention Intent. You can use the pages, site section, or custom segment dimensions to categorize your pages. Look for pages with low purchase conversion rates. In our case, we find that Online Check-In and Shore Excursion (Shorex) pages have relatively lower conversion rates than other pages that are more logically associated with shopping and purchase.

![Image 6](assets/image-6.png)

It's also a good idea to look in Workspace for high traffic pages. Scan the list of high traffic pages and decide if they indicate a retention intent.

## Excluding Other Segments

Again, our Visit Intent segments need to be mutually exclusive and completely exhaustive. If you're not tired of reading this yet, you will be! For our Retention Intent segment, it's critically important to exclude Purchase Intent behaviors.

For most of us, Purchase Intent and Retention Intent are not mutually exclusive behaviors. We have guests who come to the website to manage their upcoming cruise, but also to book their next trip (thank you!). If you're a restaurant, a visitor may check their loyalty points and then place an online order.

Even though the behavior is not mutually exclusive, our segments must be for Customer Journey analysis. We can build other very interesting segments to analyze the overlap between purchase and loyalty behaviors. But for our current purposes, we need these segments to be mutually exclusive.

Since demand generation is one of marketing's main objectives, our Retention Intent segment will exclude Purchase Intent. In other words, if somebody comes to our site to manage a cruise, but also indicates intention to book a new cruise, that visit will go to the Purchase Intent segment.

### The Retention Intent Segment in Segment Builder

Our segment definitions are becoming a bit more gnarly. Include Visits in your segment. Add your Retention Intent signals. For me, this was straightforward. If the page name starts with "bge:" (our booked guest pages), you're in the segment. I added page views is greater than one for extra measure (but we'll still exclude one hit wonders below).

Then add exclude containers for your One Hit Wonders and Purchase Intent visits. Make sure your containers are joined with the "And" condition.

![Image 7](assets/image-7.png)

Once again, look at your Visit Intent Data Quality Workspace to ensure your segments are mutually exclusive. Our Visit Intent segments are taking shape nicely!

![Image 8](assets/image-8.png)

At this point, we've configured three of our five Visit Intent segments. We see these segments are mutually exclusive. In our next post, we'll create the final Visit Intent segments, Consideration and Awareness, and our segments will all be completely exhaustive. Once our Visit Intent segments are set up, we'll bring them together into visitor-based segments that you'll find very useful for analysis and personalization.

## Author

This document was written by:

![Aaron Fossum](assets/aaron-headshot-small.png)

**Aaron Fossum**, Director, Digital Analytics

Adobe Analytics Champion
