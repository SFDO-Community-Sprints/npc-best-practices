---
layout: default
title: Program with Monetary Benefit 
nav_order: 5
parent: Program Use Cases
---

# Program with Monetary Benefit 

**Definition:** 
Programs where participants receive monetary assistance as part of their engagement. This may involve registration, eligibility verification, and tracking of disbursed funds. Participants will have some level of personal information tracked for payment purposes. The amount of the monetary assistance needs to be known but various methods can be used. The money may be paid to the participant or to a third party on their behalf. 

**Examples:**



* A housing assistance program provides rental subsidies, requiring participants to apply and meet financial eligibility criteria.
* A nonprofit scholarship program offers tuition assistance and tracking disbursements.
* A financial aid program provides cash stipends to low-income families for essential needs, maintaining records for accountability.
* A foodbank provides grocery gift cards of varying values based on family size.

**Prerequisites for Salesforce Admin:**

Required



* Overall requirements met

**Prerequisites for End User:**

Required



* Unit of Measure is set as financial amount

Optional  



* Set up Benefit Schedules with start/end dates and times 
    * Set up Benefit Sessions with frequency/recurrence, if needed

**Best Practices:**



* Defining intake or validation requirements prior to set up will determine how record creation should occur in Salesforce
* Instead of Program Management, you may want to review the core capabilities of Grantmaking for this use case as it includes: 
    * Portal for application process and reporting
    * Intense application and review process
    * Detailed tracking of fund disbursements

**How to enter data (recommended):**



* To add participant to all Benefit Sessions for a specific Benefit Schedule, use Benefit Schedule > “Add Participant” button 
    * Creates Benefit Assignment and Benefit Disbursement records with default Disbursement Status and Program Enrollment record if not already created
    * Update Disbursement Status once attendance is complete
* To add participant to a specific Benefit Session only, use Benefit Session  > “Add Participant” button 
    * Creates Benefit Assignment and Benefit Disbursement records with default Disbursement Status and Program Enrollment record if not already created
    * Update Disbursement Status once attendance is complete

**How to enter data (other options):**



* Record creation via Salesforce automation (screen flows, OmniStudio)
* Record creation via third-party form tool
* Record creation via data import tool
    * NOTE: The Data Import Wizard does not work with Nonprofit Cloud objects.
