---
layout: default
title: Data Processing Engine
nav_order: 1
parent: Industry Common Components
---
# Data Processing Engine

Audience: Salesforce admins at nonprofits and consulting partners

Goal: Enable someone to get started with Data Processing Engine.

## What is Data Processing Engine?

Data Processing Engine (DPE) is a declarative feature available with the new Nonprofit Cloud (as well as some other industry clouds) to process and manipulate large volumes of data efficiently. It uses configuration-based rules and flows to handle very large volumes of data that might cause timeouts with, say, Apex-based calculations. Calculations are offloaded for processing to either the CRM Analytics or Data Cloud platforms, depending on the configuration you choose. The results are then used to update your Salesforce records.

For nonprofits, DPE is used to make calculations about donors and donations; program participation and service delivery; and Accounting Subledger transactions.

As you dive into DPE, it can get complex very quickly—don’t panic! You can set up the standard DPE definitions with general admin skills, and we have resources to help you get started. 

## When and where DPE is used in NPC

Several DPE definition templates are provided out-of-the-box with NPC. We recommend using these templates. They are relatively easy to set up and provide very helpful summary information for users. Note that some templates may not be visible until you enable the corresponding feature set, such as Fundraising. Currently, all the out-of-the-box Nonprofit Cloud DPE definitions use CRM Analytics for processing. 

Fundraising DPE Templates:


* [DonorGiftSummary](https://help.salesforce.com/s/articleView?id=sfdo.fundraising_track_gift_donor_trends_rollups.htm&type=5)
* [GiftDesignation](https://help.salesforce.com/s/articleView?id=sfdo.fundraising_track_gift_donor_trends_rollups.htm&type=5)
* [OutreachSummary](https://help.salesforce.com/s/articleView?id=sfdo.fundraising_track_outreach_trends_with_rollups.htm&type=5)
* [Recency, Frequncy, Monetary Value Fundraising Scoring](https://help.salesforce.com/s/articleView?id=sfdo.fundraising_set_up_rfm_scoring.htm&type=5)
* [Fundraising Account Actionable List Template ](https://trailhead.salesforce.com/content/learn/projects/fundraising-portfolios-with-actionable-lists) 
* Help documentation for this one is not nonprofit-specific: [Creating Actionable Lists by Using Actionable Segmentation](https://help.salesforce.com/s/articleView?id=sf.actionable_segmentation.htm&type=5) 

Program and Benefit Management DPE Templates:

* [Aggregate Benefit Assignment and Benefit Disbursement](https://help.salesforce.com/s/articleView?id=ind.prog_case_mgmt_prog_mgmt_summary_calc.htm&type=5)
* [Aggregate Program Enrollment](https://help.salesforce.com/s/articleView?id=ind.prog_case_mgmt_prog_mgmt_summary_calc.htm&type=5)

Accounting Subledger DPE Templates:

* [Accounting Subledger Processes](https://help.salesforce.com/s/articleView?id=sfdo.asl_jobs.htm&type=5)

