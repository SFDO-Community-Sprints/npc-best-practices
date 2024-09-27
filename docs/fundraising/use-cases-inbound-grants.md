---
layout: default
title: Inbound Grants
nav_order: 5
parent: Fundraising Use Cases
---

# Inbound Grants
*Last Updated:*

Represented by Opportunity, Gift Transaction, Gift Commitment, and Gift Commitment Schedule. 

**Definition:**



* Grants are donations that typically have an application process. They are considered solicited. 
* They could be renewals of previous grants
* Payment could be made in a lump sum or several payments over time

**Examples:**



* Receive a grant paid in a lump sum by check
* Receive a grant in multiple payments over time

**Considerations:**



* Tasks may be associated with each stage of the grant process. There may be application and post-award requirements, such as LOI (application), or Reports (post-award) which need to be tracked. [Action Plans](https://help.salesforce.com/s/articleView?id=sf.fsc_action_plans.htm&type=5) may be used to track these tasks.

**Using Opportunity / Gift Commitment / Gift Commitment Schedule because:**



* Want to track solicitation process
* May be a multi-payment commitment
* May be awarded before paid, which needs to be tracked

**Prerequisites for Salesforce Admin:**



* See [Prerequisites for Salesforce Admin](https://docs.google.com/document/d/1R4sRRd1VSMeSmUbVenMY6ci_GE0FLp_FR0fYu99xvYs/edit#bookmark=id.ds0z7f6syy7y) from Use Case #2
* Required
    * On Opportunity object
        * Determine and set up the grant solicitation process (record type, stage values, Sales Process)
        * Determine and create custom fields to capture grant-specific information
        * Set up grant-specific Page Layout
    * Set up Permission Set for anyone who needs access to grant-related functionality and assign to appropriate users
* Optional
    * Set up [Action Plans](https://help.salesforce.com/s/articleView?id=sf.fsc_action_plans.htm&type=5) to track grant requirements/deliverables
    * Create automation to simplify requirement/deliverable management
    * Set up automation to create Gift Commitment from Opportunity when grant is awarded

**Prerequisites for End User:**



* See [Prerequisites for End User](https://docs.google.com/document/d/1R4sRRd1VSMeSmUbVenMY6ci_GE0FLp_FR0fYu99xvYs/edit#bookmark=id.5m49q85t9gqk) from Use Case #2

**Best Practices:**



* See [Best Practices](https://docs.google.com/document/d/1R4sRRd1VSMeSmUbVenMY6ci_GE0FLp_FR0fYu99xvYs/edit#bookmark=id.yiq4ie45xakc) from Use Case #2
* Any written documents around grant distribution/award can be tracked against Gift Commitment

**How to enter the payment via Gift Entry:**



* See [How to enter the gift via Gift Entry](https://docs.google.com/document/d/1R4sRRd1VSMeSmUbVenMY6ci_GE0FLp_FR0fYu99xvYs/edit#bookmark=id.4h03b9rj3yn) from Use Case #2

**How to enter the payment (without Gift Entry):**



* See [How to enter the gift (without Gift Entry)](https://docs.google.com/document/d/1R4sRRd1VSMeSmUbVenMY6ci_GE0FLp_FR0fYu99xvYs/edit#bookmark=id.jvrs20w0kfak) from Use Case #2
