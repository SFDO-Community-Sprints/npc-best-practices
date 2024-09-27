---
layout: default
title: Leveraging Campaigns
nav_order: 2
parent: Fundraising 
---

# Leveraging Campaigns

Represented by Campaign and [Outreach Source Codes](https://help.salesforce.com/s/articleView?id=sfdo.NPC_FR_Outreach_Source_Code_Campaigns.htm&type=5) \
 \
**Definition: **



* Fundraising campaigns that incorporate multiple types of appeals and/or communication channels

**Examples:**



* Giving Tuesday
* End-of-year fundraising 
* Capital campaign

**Prerequisites for Salesforce Admin:**



* See [Prerequisites for Salesforce Admin](https://docs.google.com/document/d/1R4sRRd1VSMeSmUbVenMY6ci_GE0FLp_FR0fYu99xvYs/edit#bookmark=id.gx3dedhygoag) from Use Case #1
* Required
    * Remove “Campaign Statistics” section from Campaign page layout (e.g. Responses in Campaign, Opportunities in Campaign, etc.)
    * Ensure the following related lists are displayed on the Campaign page layout:
        * Outreach Source Codes
        * Gift Default Designations
    * Under Setup → Data Processing Engine (DPE), ensure that there is a clone of the “OutreachSummary” job (e.g. OutreachSummary Clone). This is the DPE that will be run in order to update the Outreach Summary roll-ups on the Campaign.

**Prerequisites for End User:**



* See [Prerequisites for End User](https://docs.google.com/document/d/1R4sRRd1VSMeSmUbVenMY6ci_GE0FLp_FR0fYu99xvYs/edit#bookmark=id.knb9325eefm8) from Use Case #1
* Required
    * Create a new Campaign record, which will be used as the top-level Campaign (e.g. Giving Tuesday 2024)
    * Create Outreach Source Codes for each appeal (e.g. Email #1 - Lapsed Donors, Email #1 - Sustainers, LinkedIn Ad, Email #2 - Lapsed Donors, Direct Mail Version A, Direct Mail Version B)
* Optional
    * Assign Default Gift Designation(s) to the Campaign


<p align="center">

<img src = "/docs/assets/images/LeveragingCampaigns1.png" height="500" width= "1125">

<img src = "/docs/assets/images/LeveragingCampaigns2.png" height="500" width= "1125">

 </p>
 
 **Best Practices:**



* For online giving, follow the guidance from your donation platform provider to attach gifts to the appropriate Campaign(s) and Outreach Source Code(s).
* For offline giving, use Gift Entry to create Gift Transaction records (can handle batches). On the Gift Entry screen, select the appropriate Campaign and Outreach Source Code for attribution.
