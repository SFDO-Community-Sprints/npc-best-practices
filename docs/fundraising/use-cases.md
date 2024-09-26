---
title: Fundraising Use Cases
parent: Fundraising
nav_order: 1
---
# Fundraising Use Cases
Last Updated: 
### **Overall Considerations**

* Gift Commitments
    * When using Gift Entry to update that a Gift Transaction was paid against an existing Gift Commitment with a Gift Commitment Schedule, note that only one payment can be recorded per Gift Transaction. If the payment is lower than the expected Gift Transaction amount, the Gift Transaction will still retain the same name (i.e. the name will reflect the expected amount instead of what was actually paid). Once Gift Entry has processed the Gift Transaction, any edits will require multiple steps and manipulation of the Gift Transaction status.
    * Only one gift entry can be applied per gift commitment transaction. Gift entries of lower amounts can be applied to a commitment transaction of a higher amount. Once a gift commitment is applied to a gift entry, it cannot be removed (Gift Processing Status = Success). Gift Transaction will autoname to the commitment amount, even if the entry amount is different (based on default). Gift Transaction can be edited, but it requires multiple steps and manipulation of the status.
    * In order for the Gift Commitment to appear in Gift Entry it must meet the following criteria:
        * Effective Start Date must be populated
        * Status must be Active
        * Transaction Due Date on scheduled Gift Transaction must match Gift Received Date selected on Gift Entry
    * Gift Commitment must have an effective start date populated for the Gift Commitment to populate on gift entry.
* Gift Batching
    * To remove an entry from a batch, edit from the entry page. Using delete from the batch screen will delete the entry entirely.
    * "Set as Default" checkbox will autofill all fields exactly as set (including donor information) for each gift. Default will remain even if you exit and then return to the batch.
* Deleting 
    * Deleting a gift entry does not automatically delete the related transaction.  The transaction must be deleted separately.
* Other
    * Default automation: Transaction status will be “pending” after entry, except for a cash payment which will have a status of “paid”.
* Gift Designations
    * Be aware of [the inheritance hierarchy for Gift Designations](https://help.salesforce.com/s/articleView?id=sfdo.npc_fr_manage_designations.htm&type=5).

### **Use Case #1: Single Payment Gift - Untracked Solicitation (Final)**

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
