---
layout: default
title: Anonymous Program Participation 
nav_order: 4
parent: Program Use Cases
---

# Anonymous Program Participation 
**Definition:** 

Programs where no personal information is collected from participants. The organization only tracks the number of people served and/or the volume of services/goods provided. All of the disbursements can be given on the same date or multiple dates. All of the disbursements can be given at the same location or multiple locations. 

**Assumptions**: 



* The org tracks anonymous program participation and non-anonymous participation across different programs.. 
* Need to determine what metrics matter (i.e. # of participants/recipients, # of benefits provided, by date, by location, etc)
* Tracking Disbursement: Available/ Already spent, tracking for same date/ site?

**Examples:**



* A youth development organization runs a Summer Backpack Program, tracking how many backpacks are distributed but not who receives them.
* A food assistance program tracks the number of meals distributed, without collecting participant details.
* A literacy nonprofit hosts monthly author events, recording the total number of attendees.

**Not using Person Account because:**

* Are not tracking any identifiable information 

**Prerequisites for Salesforce Admin:**

Required



* Overall requirements met

**Prerequisites for End User:**

Required



* Set up program specific information
    * Program or Benefit
    * Program Enrollment
        * Is Anonymous = TRUE (box is checked)
        * Is Active = TRUE (box is checked)

Optional



* Set up program specific information
    * Set up Benefit Schedules with start/end dates and times
    * Set up Benefit Sessions with frequency/recurrence 

**Best Practices:**



* Create anonymous program enrollments as part of program creation process to ensure accurate data entry
* Remove unneeded fields from program enrollment page layout

**How to enter data (recommended):**



* Use the quick action button “New Ad Hoc Bulk Disbursement” from Program or Benefit record page
    * Choose Recipient Type > Anonymous
    * Number of Recipients - can add more than one person at a time
    * All disbursed on same date (cannot set time)
    * Creates Benefit Assignment and Benefit Disbursement records with default Disbursement Status and Program Enrollment record if not already created
    * Update Disbursement Status when completed

**How to enter data (other options):**



* Record creation via Salesforce automation (screen flows, OmniStudio)
* Record creation via third-party form tool
* Record creation via data import tool
    * NOTE: The Data Import Wizard does not work with Nonprofit Cloud objects.

