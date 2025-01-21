---
layout: default
title: In-Kind Gift
nav_order: 6
parent: Fundraising Use Cases
---

# In-Kind Gift


Represented by Gift Transaction 
* Gift Commitment / Gift Commitment Schedule / Opportunity optional

**Definition:**



* May or may not be solicited specifically - could have been part of a larger marketing effort
* May or may not be scheduled
* Could have a previous commitment

**Examples:**



* Products donated as part of a sponsorship
* Products donated to a food bank
* Clothing or household goods donated to a thrift store

**When to use Opportunity or Gift Commitment:**



* Tracking solicitation
* This gift is part of a mixed/multi-payment commitment
* Promised ahead of time

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

* Set Payment Method for the gift to In-Kind

**How to enter the gift via Gift Entry (recommended):**



* See How to enter the gift via Gift Entry from [Multiple Payment Gift](use-cases-multiple-payment-gift.md)

* Set Payment Method to In-Kind
* Optional
    * Create a separate template for In-Kind to allow for different fields to be specified (e.g. Quantity) that may not be applicable for other types of gifts.

**How to enter the gift (without Gift Entry):**



* See How to enter the gift (without Gift Entry) from [Multiple Payment Gift](use-cases-multiple-payment-gift.md)

**Special Considerations**
* A Gift Transaction must have a dollar amount greater than $0 so you cannot enter an in-kind Gift Transaction for $0. Using the amount field on the Gift Transaction for the fair market value will mean the gift ends up being counted as a regular gift in rollups. There are two suggested solutions:
    * Create a custom fair market value field on Gift Transaction and enter $0 in the amount field OR
    * Use the amount field for the fair market value and alter the Donor Gift Summary Data Processing Engine definition to exclude in-kind gift transactions.

