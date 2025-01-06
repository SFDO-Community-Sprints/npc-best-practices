---
layout: default
title: Matching Gift
nav_order: 4
parent: Fundraising Use Cases
---

# Matching Gift


Represented by one Gift Transaction, linked to another Gift Transaction

**Definition:**



* A gift (the “Matching Gift Transaction”) that is intended to match other donation(s) (the “Matched Gift(s)”), potentially dollar-for-dollar, sometimes up to a certain amount
* Not scheduled
* No previous commitment

**Examples:**



* Employer matches employee giving over a period of time
* One donor encourages holiday giving by offering to double donation amounts up to a goal amount

**Not using Opportunity or Gift Commitment because:**



* See Not using Opportunity or Gift Commitment from [Single Payment Gift - Untracked Solicitation](use-cases-single-payment-gift-untracked-solicitation.md)
* Matching gifts are typically a one-time gift

**Prerequisites for Salesforce Admin:**



* See Prerequisites for Salesforce Admin from [Single Payment Gift - Untracked Solicitation](use-cases-single-payment-gift-untracked-solicitation.md)
* Optional
    * Create a custom field at the Bsuiness Account level to capture matching policies for the matching gift donor.
    * Create a roll-up summary totalling the amounts of all related Matched Gift Transactions onto the Matching Gift Transaction (using [DLRS](https://sfdo-community-sprints.github.io/DLRS-Documentation/) or [OmniStudio](https://help.salesforce.com/s/articleView?id=sf.os_omnistudio.htm&type=5)) 
    * In order to display all related Gift Transaction records on the Matching Gift Transaction record, use [ARC](https://help.salesforce.com/s/articleView?id=sf.fsc_admin_arc_overview.htm&type=5), reports, or [Timeline](https://help.salesforce.com/s/articleView?id=sfdo.NPC_PM_Set_Up_a_Timeline.htm&type=5)

**Prerequisites for End User:**



* See Prerequisites for End User from [Single Payment Gift - Untracked Solicitation](use-cases-single-payment-gift-untracked-solicitation.md)

**Best Practices:**



* After the matching gift is entered, link it to the relevant initial donation(s). Update the “Matching Employer Transaction” lookup on the Gift Transaction record(s) representing the initial donation(s) with the newly created matching gift.

**How to enter the gift via Gift Entry (recommended):**



* See How to enter the gift via Gift Entry from [Single Payment Gift - Untracked Solicitation](use-cases-single-payment-gift-untracked-solicitation.md)

**How to enter the gift (without Gift Entry):**



* See How to enter gift (without Gift Entry) from [Single Payment Gift - Untracked Solicitation](use-cases-single-payment-gift-untracked-solicitation.md)
