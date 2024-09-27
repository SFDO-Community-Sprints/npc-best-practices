---
layout: default
title: Multiple Payment Gift
nav_order: 2
parent: Fundraising Use Cases
---

# Multiple Payment Gift
*Last Updated:*

Represented by Gift Transactions and Gift Commitment (Gift Commitment Schedule optional, Opportunity optional)

**Definition:**



* Not explicitly solicited - could have been part of a larger marketing effort
* Could have a previous commitment

**Examples:**



* Could be pledge
* Could be a Letter of Intent

**Optional Opportunity because**:



* Tracking solicitation may not be necessary

**Optional Gift Commitment Schedule because**:



* Schedule does not follow a pattern

**Prerequisites for Salesforce Admin:**



* See Prerequisites for Salesforce Admin from [Single Payment Gift - Untracked Solicitation](fundraising/single-payment-gift---untracked-solicitation)
* Required
    * Set intervals for General Fundraising Settings - this enables Gift Commitments to be available for selection within Gift Entry
* Optional
    * Determine naming convention for Gift Commitments, and set up corresponding automation
    * Customize the Gift Commitment object (e.g. record types, picklists, custom fields, page layouts, Lightning pages)
    * Set up and customize the Gift Commitment Schedule object
    * Set up and customize the Payment Instrument object

**Prerequisites for End User:**



* See Prerequisites for End User from [Single Payment Gift - Untracked Solicitation](single-payment-gift---untracked-solicitation)

* Required
    * Ensure Person/Business Account exists for the donor first if not using GIft Entry

**Best Practices:**



* See [Best Practices](https://docs.google.com/document/d/1R4sRRd1VSMeSmUbVenMY6ci_GE0FLp_FR0fYu99xvYs/edit#bookmark=id.vt2sd1ngg4v) from Use Case #1
* Create an Opportunity when a potential gift is identified.
* Create Gift Commitment when the donor has committed to the gift.
    * Use Formal Commitment Type to communicate either verbal or written commitment.
* Create Gift Transaction through Gift Entry when payment is received.

**How to enter the gift via Gift Entry (recommended):**



* See [How to enter the gift via Gift Entry](https://docs.google.com/document/d/1R4sRRd1VSMeSmUbVenMY6ci_GE0FLp_FR0fYu99xvYs/edit#bookmark=id.1e6ubmrzs3at) from Use Case #1
* Can select existing Gift Commitment from this screen
    * If Gift Commitment exists for that donor and a transaction for it is due within the interval set in the Fundraising General Settings, it will be available to match the transaction to.
    * It may be easier to have the Gift Commitment and Gift Commitment [Schedule](https://help.salesforce.com/s/articleView?id=sfdo.NPC_FR_Schedule_Gift_Commitments.htm&type=5) created first if this is the first payment on a donation but will depend on ease of workflow for your organization

**How to enter the gift (without Gift Entry):**



* Create a new Gift Commitment record
    * [Optional] Click [Manage Gift Commitment Schedule](https://help.salesforce.com/s/articleView?id=sfdo.NPC_FR_Schedule_Gift_Commitments.htm&type=5) to create a new Gift Commitment Schedule
    * [Optional] Click [Manage Gift Default Designations](https://help.salesforce.com/s/articleView?id=sfdo.NPC_FR_Manage_Gift_Default_Designations_Gift_Commitment.htm&type=5) to set default designations.
* See [How to enter the gift (without Gift Entry)](https://docs.google.com/document/d/1R4sRRd1VSMeSmUbVenMY6ci_GE0FLp_FR0fYu99xvYs/edit#bookmark=id.vmcuyvd78uwj) from Use Case #1
    * When creating the Gift Transaction, select the newly created Gift Commitment (and Gift Commitment Schedule)
