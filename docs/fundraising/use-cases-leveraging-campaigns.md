---
layout: default
title: Leveraging Campaigns
nav_order: 2
parent: Fundraising 
---

# Leveraging Campaigns

Fundraising campaigns in NPC incorporate multiple types of appeals and/or communication channels.  They are represented by Campaign and [Outreach Source Codes](https://help.salesforce.com/s/articleView?id=sfdo.NPC_FR_Outreach_Source_Code_Campaigns.htm&type=5)


**Examples:**
* Giving Tuesday
* End-of-year fundraising 
* Capital campaign

**Prerequisites for Salesforce Admin:**

See Prerequisites for Salesforce Admin on [Single Payment Gift - Untracked Solicitation](use-cases-single-payment-gift-untracked-solicitation.md)
* Required Steps: 
    * Remove “Campaign Statistics” section from Campaign page layout (e.g. Responses in Campaign, Opportunities in Campaign, etc.)
    * Ensure the following related lists are displayed on the Campaign page layout:
        * Outreach Source Codes
        * Gift Default Designations
    * Under Setup → Data Processing Engine (DPE), ensure that there is a clone of the “OutreachSummary” job (e.g. OutreachSummary Clone). This is the DPE that will be run in order to update the Outreach Summary roll-ups on the Campaign.

**Prerequisites for End User:**
See Prerequisites for End User on [Single Payment Gift - Untracked Solicitation](use-cases-single-payment-gift-untracked-solicitation.md)
* Required Steps:
    * Create a new Campaign record, which will be used as the top-level Campaign (e.g. Giving Tuesday 2024)
    * Create Outreach Source Codes for each appeal (e.g. Email #1 - Lapsed Donors, Email #1 - Sustainers, LinkedIn Ad, Email #2 - Lapsed Donors, Direct Mail Version A, Direct Mail Version B)
* Optional
    * Assign Default Gift Designation(s) to the Campaign


![A listview of Source Codes for Campaigns connected to the 2024 Giving Tuesday Campaign. The listview contains the Campaign Name, Campaign Status, and Source Code.](https://github.com/user-attachments/assets/006779e6-f43e-4bf1-a973-326d5a0292b6)

Listview of Source Codes for Campaigns connected to the 2024 Giving Tuesday Campaign. The listview contains the Campaign Name, Campaign Status, and Source Code.

![The 2024 Giving Tuesday Campaign record. Outreach Source Codes are listed on the right sidebar](https://github.com/user-attachments/assets/fa827212-6137-4143-b6e2-28cc822489c9)

2024 Giving Tuesday Campaign record. Outreach Source Codes are listed on the right sidebar.

 
 **Best Practices:**

* For online giving, follow the guidance from your donation platform provider to attach gifts to the appropriate Campaign(s) and Outreach Source Code(s).
* For offline giving, use Gift Entry to create Gift Transaction records (can handle batches). On the Gift Entry screen, select the appropriate Campaign and Outreach Source Code for attribution.
