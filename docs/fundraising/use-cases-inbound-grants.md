---
layout: default
title: Inbound Grants
nav_order: 5
parent: Fundraising Use Cases
---

# Inbound Grants

Represented by Opportunity, Gift Transaction, Gift Commitment, and Gift Commitment Schedule. 

**Definition:**

* Grants are donations that typically have an application process. They are considered solicited. 
* They could be renewals of previous grants.
* Payment could be made in a lump sum or several payments over time.

**Examples:**

* Receive a grant paid in a lump sum by check
* Receive a grant in multiple payments over time

**Considerations:**

* Tasks may be associated with each stage of the grant process. There may be application and post-award requirements, such as LOI (application), or Reports (post-award) which need to be tracked. [Action Plans](https://help.salesforce.com/s/articleView?id=sf.fsc_action_plans.htm&type=5) may be used to track these tasks but they must be on the Opportunity.

**Using Opportunity / Gift Commitment / Gift Commitment Schedule because:**



* Want to track solicitation process
* May be a multi-payment commitment
* May be awarded before paid, which needs to be tracked

**Prerequisites for Salesforce Admin:**



* See Prerequisites for Salesforce Admin from [Multiple Payment Gift](use-cases-multiple-payment-gift.md)

* Required
    * On the Opportunity object:
        * Determine and set up the grant solicitation process (record type, stage values, Sales Process)
        * Determine and create custom fields to capture grant-specific information
        * Set up grant-specific Page Layout
    * Set up Permission Set for anyone who needs access to grant-related functionality and assign to appropriate users
* Optional
    * Set up [Action Plans](https://help.salesforce.com/s/articleView?id=sf.fsc_action_plans.htm&type=5) to track grant requirements/deliverables
    * Create automation to simplify requirement/deliverable management
    * Set up automation to create Gift Commitment from Opportunity when grant is awarded

**Prerequisites for End User:**



* See Prerequisites for End User from [Multiple Payment Gift](use-cases-multiple-payment-gift.md)


**Best Practices:**



* See Best Practices from [Multiple Payment Gift](use-cases-multiple-payment-gift.md)

* Any written documents around grant distribution/award can be tracked against Gift Commitment

**How to enter the payment via Gift Entry:**



* See How to enter the gift via Gift Entry from [Multiple Payment Gift](use-cases-multiple-payment-gift.md)


**How to enter the payment (without Gift Entry):**



* See How to enter the gift (without Gift Entry) from [Multiple Payment Gift](use-cases-multiple-payment-gift.md)

