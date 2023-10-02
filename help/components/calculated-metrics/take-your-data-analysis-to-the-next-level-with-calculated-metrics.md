---
title: Take your data analysis to the next level with Calculated Metrics
description: Learn how a peer expert uses Calculated Metrics to create new metrics without changing their implementation and using the data already collected to help answer complex business questions.
feature: Calculated Metrics
role: User
level: Beginner
doc-type: Article
last-substantial-update: 2023-05-16
jira: KT-13266
thumbnail: KT-13266.jpeg
exl-id: 74793149-9967-4765-832c-c65e578ee34b
---
# Take your data analysis to the next level with Calculated Metrics

Most new users of Adobe Analytics are familiar with Segments as a way to slice and dice their data. Today, I want to introduce you to calculated metrics, the next best tool in your analyst toolbox.

As an advanced feature of Adobe Analytics, calculated metrics let you create new metrics without changing your implementation using the data you've already collected. The Calculated Metrics Builder can use a lot of different mathematical and statistical functions, so you can create metrics that answer even the most complex business questions.

## Getting Started with Calculated Metrics

To get started with calculated metrics, let's look at a simple example. Imagine you want to understand if online self-serve users have a higher average order value (AOV) than call-assisted users. To build a calculated metric to answer this question, do the following:

To open the Calculated Metrics Builder, use the top navigation to click → **Components** → **Calculated Metrics** → **+ Add.** Or, you can click the **+ sign** above **Metrics** in the Components panel. 


![Calc 01](assets/calc01.png) ![Calc 02](assets/calc03.png) ![Calc 03](assets/calc02.png)

![Calc 04](assets/calc04.png)  

*Descriptions below for UI items*

Once the Calculated Metrics Builder opens, add and/or do the following:

**A.** A name for your calculated metric. This name is displayed in the metrics components list, so make it something that will be clear to yourself and others, like *Call Center AOV*.

**B.** A description of the calculated metric. This description appears when users click the '**i**' beside the metric in the components list, so be sure it's informative. For example, for Call Center AOV, we might add *Calculates AOV for Call Center Assisted Orders*.

**C.** The metric format: Pick decimal, time, percent or currency, and add decimal places and polarity. Here, we'll pick *Currency for the Format, 0 for number of decimals, and* ⬆ *Good (Green) for polarity.*

**D**. If you're using tags, which allow you to apply topics and quickly locate calculated metrics, add the tag(s) that apply here. We've added *AOV* and *Call Center* tags.

**E.** This section is for display - as you build your calculated metric in section F, the formula will show here.

**F.** Here, you'll drag and drop dimensions (H), metrics (I) or segments (J) to create your calculated metric as well as the operators for the formula. For each metric, if you click the cog wheel, you can change the Metric Type (Standard/Total) and Attribution Model. *We'll drag and drop Call Center Revenue, then below that, we'll*÷￼*. We will accept the default metric type and attribution model.*

**G**. Use this **+Add** option to add additional conditions or static numbers, which we don't need here.

**K.** And finally, as you build your calculation, you can preview the past 90 days' data here.

Now that we've built Call Center AOV, we also need a calculated metric for Online AOV. We would do this following the same steps outlined above.

Next, we can build a third calculated metric, either using the Calculated Metrics Builder or on the fly from within the freeform table, to compare the Call Center and Online AOV so we end up with something like this:

![Calc 05](assets/calc05.png)

In our example, we see a significant lift when shoppers use the call center to help them make a purchase. This data can then inform our decisions about how to help customers get assistance with their purchases through, for example, popup offers or other guided experiences.

## Using Segments in Calculated Metrics

Now, let's look at how we can use segments in calculated metrics to gain more insight into customer behavior, preferences, and motivations. With segments and calculated metrics, we can learn enough about customers to improve their experience, increase revenue, and improve customer satisfaction and loyalty.

We already know from the above AOV examples that call center assisted purchases typically have a higher AOV. However, other metrics tell us that most users don't use the call center for purchases. 

So, which retail categories - and user paths through those categories - result in the highest AOV?  We can find out by combining segments with calculated metrics. 

To do so, we first need to create visit-level *include* and *exclude* segments for each product category. Include or exclude is determined by clicking the **Options** gear in the right corner of the container. Default is Include.

![Calc 06](assets/calc06.png) ![Calc 07](assets/calc07.png)

Once we've created these segments, we can create a calculated metric to give you the answer to your question. We open the Calculated Metrics Builder and do the following:

1. Search for the newly created segments and drag and drop the ones we want to use into the gray area at the top of the **Definition** box. For example, if we want to create an AOV for users who visited both Women's and Men's categories, but not Kid's, we can drag and drop these three segments to that area: *Include Women's*, *Include Men's*, and *Exclude Kid's*. We call this *stacking segments*.

    ![Calc 09](assets/calc09.png) ![Calc 08](assets/calc08.png) 

1. Then, we drag and drop the **Online Revenue** metric into the same container, then **Online Orders**. Since containers work like mathematical expressions to determine order of operations, items in containers are processed before subsequent processes, though we don't have multiple containers or processes in this calculation.
1. We change the operator between the two metrics to division (÷).
1. We Select **Currency** as the format, **0** decimal places, and **UP** for polarity.
1. Name the calculated metric and provide a description.
1. Save.

When we're done, our calculated metric looks like this: 

![Calc 10](assets/calc10.png)

After we create calculated metrics using stacked segments for each combination of visitor's category journey and take a look at the data, look at what we learn! Users who visit both the Women's and Men's categories during their visit have the highest AOV and when compared to visitors of a single category, the lift is significant:

![Calc 11](assets/calc11.png) ![Calc 12](assets/calc12.png)

Knowing this, we can optimize page layout, product placements, and promotional messaging to get more people into these categories before checking out. 

## Valuable, but not Available Everywhere

**So - calculated metrics, both simple and complex, are super valuable for analysts!** 

However, these metrics are not available in all areas of Adobe Analytics. You can't use calculated metrics in:

- Fallout in Analysis Workspace
- Cohort Analysis in Analysis Workspace
- Data Warehouse
- Real Time reports
- Current Data reports
- Analytics for Target
- Report Builder
 
## Calculated Metrics Best Practices

Now that you know how valuable calculated metrics can be, let's take a look at some best practices in building them.

1. **Check your formula syntax.** Make sure the formula syntax is both correct and follows the Adobe Analytics syntax to make sure you get meaningful information.
1. **Verify the order of operations.** Make sure to use containers carefully and put things in proper mathematical order of operations.
1. **Don't double-count data**. You can avoid double-counting data by ensuring that the formula used in the calculated metric doesn't count the same data multiple times. This is often achieved by combining *Include* and *Exclude* conditions in the calculated metric or through the use of segments.
1. **Check time granularity.** Make sure the calculated metric has the same time granularity as the source metrics used in the formula.
1. **Use accurate data:** You'll only get valuable results if you use accurate and reliable data in the calculation.

## Custom Segment Best Practices

When creating segments in Adobe Analytics, keep these best practices in mind:

1. **Keep it simple.** Avoid overcomplicating the segment. Keep it as simple as possible and use only the conditions necessary to ensure accuracy.
1. **Use the correct container types**. Make sure to use the correct container type - visitor, visit, or hit - in the segment definition to avoid getting incorrect results.
1. **Don't double-count data**. Like with calculated metrics, ensure the segment doesn't count the same data multiple times. Include and Exclude containers can help.
   1. When an include container is used, it *includes* *all the content of the visit* if any hit matches the condition within the visit. 
   1. When an exclude container is used, it *excludes all the content of the visit* if any hit matches the condition within the visit. 
1. **Nest containers properly**. Determine what data is included using the outermost container, then apply nested rules to the remaining data. As nested rules are applied, the segment flow acts as a funnel, and subsequent rules do not apply to any hits that the first rule excluded.
1. **Make sure your data is up to date.** Make sure to use accurate and up-to-date data in the segment definition to get accurate results.
1. **Test the segment.** Always test the segment to make sure it's working as intended before releasing it to others.
1. **Consider performance.** Segments may slow down report processing, so consider that impact when building them.

## Key Takeaways

Combining segments and calculated metrics in Adobe Analytics can absolutely lead to more robust and effective data analysis. By slicing and dicing your data and building calculations for comparison, you can gain deeper insights into customer behavior that you can use to optimize your marketing campaigns and create tailored dashboards and reports. However, remember that calculated metrics aren't available in all areas of Adobe Analytics, and make sure to follow best practices to ensure you're getting accurate and useful data.


## Author

This document was written by:

![Debbie Kern](assets/calc13.jpeg)

**Debbie Kern**, Senior Adobe Analytics Manager at Adswerve

![Adswerve](assets/calc14.png)
