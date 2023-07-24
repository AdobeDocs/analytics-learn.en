---
title: Simple hacks for greater efficiency and self-service - part 1
description: Learn the key challenges analytics teams face today, and our recommendations to overcome them using strategies outside the Adobe Analytics UI.
feature: Analytics Basics
role: Admin, Leader
level: Intermediate
solution: Analytics
exl-id: 5d1077fd-d006-4a85-bf1c-54f6b2d31934
---
# Adobe Analytics: Simple hacks for greater efficiency and self-service

**Part 1: Outside the UI**

This article describes key challenges that analytics teams face today, and our recommendations to overcome them using strategies outside the Adobe Analytics interface. 

## Key challenges for Analytics teams

Many Analytics teams find themselves with an imbalanced distribution of work. Instead of a mix of 80% analysis and 20% implementation, numerous organizations find themselves in the inverse of that. They see most of their efforts spent setting up, reporting, and providing support as opposed to producing analysis that drives high value insights.

Analytics teams are finding their productivity and efficiency drained for various reasons. These include the ever-changing and evolving implementations, trying to maintain organizational trust in the data, and reducing analyst turnover. Reducing turnover avoids the lengthy process of training new team members on unfamiliar, custom-implementation tools.

Other key challenges analysts face:

* **Competition:** Online and multi-channel retail businesses grow more competitive.
* **Customer expectations:** Customer experiences and marketing strategies become more complex.
* **Data Value:** The value of accurate data and insights to drive a competitive advantage grows more important.
* **Stakeholder expectations:** Business partners, stakeholders, and executives increasingly request data before approval.
* **Project management:** The analytics team drowns in requests to implement data collection for a never-ending stream of new features, while producing accurate reports, onboarding new analysts, and uncovering the next new insight.

## Keys to efficiency: Outside the UI

1. Keep your [Solution Design Reference](/help/implementation/implementation-basics/creating-and-maintaining-an-sdr.md) (SDR) up to date:

   * The SDR is the primary source of truth for the definition and intended use of all variables within your analytics implementation.
   * The SDR is the main reference that users must be familiar with to get value out of your Adobe Analytics UI.
   * Keeping it updated and versioned (a simple date format can be used) is important.

1. Data collection documentation and governance - tech specifications:

   The tech spec has a more limited audience than the SDR but is as important, if not more, for a fully functional implementation. A good tech spec should be all the development, QA, and tag management resources needed to implement the solution. Be sure to maintain as many documents as are needed to accommodate unique implementation architectures.

   **Tech Spec**

   _Use Case:_ Instructions describing how to construct scripts for data collection

   _Primary Users:_ Developers

   _Other Notes:_

    * Highly technical document built specifically for your deployment environments
    * Useful for both initial implementation and subsequent maintenance/reference
    * Organized by solution type (for example, campaign tracking, page metadata, and so on.)
    * Primary document needs to be updated and maintained as SDR changes are made
    * Central repository
    * Synchronized version numbers for SDR and Tech Spec

1. Communicate and document solution design intent on launch:

   * Communicate with the user in mind
   * When launching or enhancing data collection, create simple summaries that can be shared with stakeholders
   * Reinforce proper variable use out of the gate
   * Send a summary launch announcement email to the main stakeholders and analysts
   * Create a library that can be used in support of office hours, team enablement sessions, or for team-specific onboarding

1. Data collection documentation, governance, and data hygiene - AHD:

   The Analytics Health Dashboard (AHD) dives deep into a _single_ report suite and provides a view into data collected in every component (eVar, prop, and event). This can help point out if data has stopped collecting into a component so you can take action to correct the issue. You can run this dashboard at any time in the future for any report suite.

   Analytics Health Dashboard (AHD):

   _Use Case:_ Snapshot of every metric and dimension being captured by a single report suite
  
   _Primary Users:_ Lead Analytics SME and/or Dev

   _Other Notes:_
    * Delivered through Excel using a custom integration of the Adobe Reporting API
    * Users must have Analytics web services API access
    * Options to semi-automate exist

1. Win through expanding the world of subject matter experts (SMEs):

   * Establish SMEs within the various teams in the organization
   * Build their presence by helping socialize releases and wins
   * Use regular office hours to help train the trainers and cut down on ad-hoc asks

Learn more about strategy and thought leadership at the [Customer Success](https://experienceleague.adobe.com/docs/customer-success/customer-success/overview.html) hub.