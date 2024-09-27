---
layout: default
title: Matching Gift
nav_order: 4
parent: Fundraising Use Cases
---

# Matching Gift
*Last Updated:*
Represented by one Gift Transaction, linked to another Gift Transaction

**Definition:**



* A gift (the “Matching Gift Transaction”) that is intended to match another donation (the “Matched Gift”), potentially dollar-for-dollar, sometimes up to a certain amount
* Not scheduled
* No previous commitment

**Examples:**



* Employer matches employee giving over a period of time
* One donor encourages holiday giving by offering to double donation amounts up to a goal amount

**Not using Opportunity or Gift Commitment because:**



* See [Not using Opportunity or Gift Commitment](https://docs.google.com/document/d/1R4sRRd1VSMeSmUbVenMY6ci_GE0FLp_FR0fYu99xvYs/edit#bookmark=id.5a667yd60mvb) from Use Case #1
* Matching gifts are typically a one-time gift

**Prerequisites for Salesforce Admin:**



* See [Prerequisites for Salesforce Admin](https://docs.google.com/document/d/1R4sRRd1VSMeSmUbVenMY6ci_GE0FLp_FR0fYu99xvYs/edit#bookmark=id.gx3dedhygoag) from Use Case #1
* Optional
    * Create a custom field to capture matching policies for the matching gift donor called “Matching Employer Transaction”
    * Create a roll-up summary totalling the amounts of all related Matched Gift Transactions onto the Matching Gift Transaction (using [DLRS](https://sfdo-community-sprints.github.io/DLRS-Documentation/) or OmniStudio) 
    * In order to display all related Gift Transaction records on the Matching Gift Transaction record, use [ARC](https://help.salesforce.com/s/articleView?id=sf.fsc_admin_arc_overview.htm&type=5), reports, or [Timeline](https://help.salesforce.com/s/articleView?id=sfdo.NPC_PM_Set_Up_a_Timeline.htm&type=5)

**Prerequisites for End User:**



* See [Prerequisites for End User](https://docs.google.com/document/d/1R4sRRd1VSMeSmUbVenMY6ci_GE0FLp_FR0fYu99xvYs/edit#bookmark=id.knb9325eefm8) from Use Case #1

**Best Practices:**



* After the matching gift is entered, link it to the relevant initial donation(s). Update the “Matching Employer Transaction” lookup on the Gift Transaction record(s) representing the initial donation(s) with the newly created matching gift.

**How to enter the gift via Gift Entry (recommended):**



* See [How to enter the gift via Gift Entry](https://docs.google.com/document/d/1R4sRRd1VSMeSmUbVenMY6ci_GE0FLp_FR0fYu99xvYs/edit#bookmark=id.1e6ubmrzs3at) from Use Case #1

**How to enter the gift (without Gift Entry):**



* See [How to enter gift (without Gift Entry)](https://docs.google.com/document/d/1R4sRRd1VSMeSmUbVenMY6ci_GE0FLp_FR0fYu99xvYs/edit#bookmark=id.vmcuyvd78uwj) from Use Case #1
