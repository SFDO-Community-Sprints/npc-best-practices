---
layout: default
title: In-Kind Gift
nav_order: 6
parent: Fundraising Use Cases
---

# In-Kind Gift


Represented by Gift Commitment
* Gift Transaction optional - see note under Best Practices.
* Opportunity optional.

**Definition:**

* May or may not be solicited specifically - could have been part of a larger marketing effort
* May or may not be scheduled
* Could have a previous commitment

**Examples:**

* Products donated as part of a sponsorship
* Products donated to a food bank
* Clothing or household goods donated to a thrift store

**When to use Opportunity:**

* Tracking solicitation
* This gift is part of a mixed/multi-payment commitment

**Prerequisites for Salesforce Admin:**

* See Prerequisites for Salesforce Admin from [Multiple Payment Gift](use-cases-multiple-payment-gift.md)

* Required
    * Review and modify Gift Vehicle picklist values on Gift Commitment, as needed
* Optional
    * Add custom field(s) for tracking description and quantity. This also needs to be added to the Gift Entry Flow, if required.

**Prerequisites for End User:**

* See Prerequisites for End User from [Multiple Payment Gift](use-cases-multiple-payment-gift.md)


**Best Practices:**

* See Best Practices from [Multiple Payment Gift](use-cases-multiple-payment-gift.md)

* NOTE: If using a Gift Transaction for in-kind gifts, set the Payment Method for the gift to In-Kind on the Gift Transaction and use the Original Amount field for the fair market value of the gift. Using a Gift Transaction will cause the gift to be inclued in the Donor Gift Summary rollups as a regular gift so you will need to exclude it. You may also wish to add in a rollup for in-kind gifts.




