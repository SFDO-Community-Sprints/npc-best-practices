---
layout: default
title: Multiple Payment Gift
nav_order: 2
parent: Fundraising Use Cases
---

# Multiple Payment Gift

Represented by Gift Transactions and Gift Commitment (Gift Commitment Schedule optional, Opportunity optional)

**Definition:**

* Not explicitly solicited - could have been part of a larger marketing effort
* Could have a previous commitment

**Examples:**

* Could be a pledge
* Could be a Letter of Intent

**Optional Opportunity because**:

* Tracking solicitation may not be necessary

**Optional Gift Commitment Schedule because**:



* Schedule does not follow a pattern

**Prerequisites for Salesforce Admin:**



* See Prerequisites for Salesforce Admin from [Single Payment Gift - Untracked Solicitation](use-cases-single-payment-gift-untracked-solicitation.md)
* Required
    * Set intervals for General Fundraising Settings - this enables Gift Commitments to be available for selection within Gift Entry
* Optional
    * Determine naming convention for Gift Commitments, and set up corresponding automation
    * Customize the Gift Commitment object (e.g. record types, picklists, custom fields, page layouts, Lightning pages)
    * Set up and customize the Gift Commitment Schedule object
    * Set up and customize the Payment Instrument object

**Prerequisites for End User:**



* See Prerequisites for End User from [Single Payment Gift - Untracked Solicitation](use-cases-single-payment-gift-untracked-solicitation.md).


**Best Practices:**



* See Best Practices from [Single Payment Gift - Untracked Solicitation](use-cases-single-payment-gift-untracked-solicitation.md)
* Create an Opportunity when a potential gift is identified.
* Create Gift Commitment when the donor has committed to the gift.
    * Use Formal Commitment Type to communicate either verbal or written commitment.
* Create Gift Transaction through Gift Entry when payment is received.

**How to enter the gift via Gift Entry (recommended):**



* See How to enter the gift via Gift Entry from [Single Payment Gift - Untracked Solicitation](use-cases-single-payment-gift-untracked-solicitation.md)
    * You can select existing Gift Commitment from this screen
    * If a Gift Commitment exists for the donor, and is within the date range set up in Fundraising - General Settings, it will be available to match the transaction to.

**How to enter the gift (without Gift Entry):**



* Create a new Gift Commitment record
    * [Optional] If the gift will be a recurring gift, click [Manage Gift Commitment Schedule](https://help.salesforce.com/s/articleView?id=sfdo.NPC_FR_Schedule_Gift_Commitments.htm&type=5) to create a new Gift Commitment Schedule
    * [Recommended] Click [Manage Gift Default Designations](https://help.salesforce.com/s/articleView?id=sfdo.NPC_FR_Manage_Gift_Default_Designations_Gift_Commitment.htm&type=5) to set default designations.
* See How to enter the gift (without Gift Entry) from [Single Payment Gift - Untracked Solicitation](use-cases-single-payment-gift-untracked-solicitation.md)
    * When creating the Gift Transaction, select the newly created Gift Commitment (and Gift Commitment Schedule)
