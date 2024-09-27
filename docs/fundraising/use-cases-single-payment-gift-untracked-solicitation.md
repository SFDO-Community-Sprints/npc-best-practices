---
layout: default
title: Single Payment Gift - Untracked Solicitation
nav_order: 1
parent: Use Cases
---

# Single Payment Gift - Untracked Solicitation

### **Single Payment Gift - Untracked Solicitation**

Represented by one Gift Transaction 

**Definition:**



* Not solicited specifically - could have been part of a larger marketing effort
* Not scheduled
* No previous commitment

**Examples:**



* Could be an online donation
* Could be cash/check/charge received one-time through mail/in-person

**Not using Opportunity or Gift Commitment because:**



* Tracking solicitation is not necessary
* This gift is not part of a multi-payment commitment
* Not promised ahead of time (or this promise does not need to be tracked)

**Prerequisites for Salesforce Admin:**



* Required
    * NPC Fundraising setup must be completed
        * [Basic setup](https://help.salesforce.com/s/articleView?id=sfdo.NPC_Set_Up_Nonprofit_Cloud.htm&type=5)
        * Fundraising setup is needed to account for Industry Common Components
        * Person Accounts and/or Business Accounts must be configured
        * Setup > Person Accounts (confirm enabled)
    * Set up [Default Designation](https://help.salesforce.com/s/articleView?id=sfdo.NPC_FR_Create_Org_Wide_Default_Other_Gift_Designations.htm&type=5) 
* Optional
    * Set Up Gift Entry
    * Determine naming convention for Campaigns, and set up corresponding automation
    * Determine naming convention for Gift Transactions, and set up corresponding automation (Note that Gift Entry **does** apply a default naming convention)
    * Review Payment Method picklist values and remove/add if required (IMPORTANT: As of June 2024, it is not possible to add values to Payment Method without errors - subscribe to [this known issue](https://issues.salesforce.com/issue/a028c00000yxpEIAAY/nonprofit-cloudnpc-fundraising-unable-to-process-gifs-in-gift-entry-with-a-custom-payment-method-picklist-value) to get updates.)
    * Set up [Source Code](https://help.salesforce.com/s/articleView?id=sfdo.NPC_FR_Outreach_Source_Code_Campaigns.htm&type=5) 
    * Remove New button for Gift Transactions (only create through Gift Entry)

**Prerequisites for End User:**



* Optional
    * Create Person/Business Account for the donor before creating Gift Transaction
    * Create Campaign
    * Create Designation
    * Create Outreach Source Code

**Best Practices:**



* Use Status field on Gift Transaction to track whether payment was successful
* For online gifts that come in that should be attached to a stewarded Gift Commitment, populate the lookup on the Gift Transaction
* Set appropriate required fields on Gift Transaction (Note that Amount and Payment Method are required by default)
* Using the Gift Entry option for entering gifts is recommended

**How to enter the gift via Gift Entry (recommended):**



* [Gift Entry](https://help.salesforce.com/s/articleView?id=sfdo.NPC_FR_Create_Gift_Entry.htm&type=5) (same experience for [batch](https://help.salesforce.com/s/articleView?id=sfdo.NPC_FR_Create_Gift_Batch.htm&type=5) vs. single gift)
    * Still need to track details that are found in Gift Entry (e.g. designation)
    * Cannot add Gift Entry to batch if it has been processed (Status = success)
* Can create donor records from this screen
* Can add a link to [Gift Commitment](https://help.salesforce.com/s/articleView?id=sfdo.NPC_FR_Gift_Commitments.htm&type=5)
    * If Gift Commitment exists for that donor, will list them
* Gives options for 
    * Link to Gift Commitment
    * Add Soft Credits
    * If you open Designation Information or Soft Credit Information and realize you don’t need them, you can delete those lines 
* Auto-naming in place
    * {Donor}-{Amount}-{Date} [test date format for locales]

**How to enter the gift (without Gift Entry):**



* [Create a new Gift Transaction](https://help.salesforce.com/s/articleView?id=sfdo.NPC_FR_Create_a_Gift_Transaction.htm&type=5) record (standard record creation)
* Auto-naming is not out-of-the-box
