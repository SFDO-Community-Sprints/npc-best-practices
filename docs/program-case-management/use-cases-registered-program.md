---
layout: default
title: Registered Program Participation (Predefined Sessions)
nav_order: 1
parent: Program Use Cases
---

# Registered Program Participation (Predefined Sessions)
**Definition:**

Tracking people who participate in a structured program that requires registration and enrollment before they receive a service or benefit. Participants commit to attending for a defined period with multiple sessions that have predefined start and end dates/times. The organization collects relevant details about the attendees. May be part of the core mission or related to the mission. May be outcome-associated or not. 

**Examples:**



* A youth development organization offers a summer learning program where students register and commit to attending for the full session.
* A human services organization provides a grief support group, where participants register for a multi-session series, and attendance is tracked.
* A community center distributes bus passes on a set schedule to low-income youth, requiring proof of age, address, and income level.
* A workforce services organization offers soft skills and job training, tracking attendance and completion rates.

**Prerequisites for Salesforce Admin:**

Required



* Overall requirements met
* Set up program specific information 
    * Set up Benefit Schedules with start/end dates and times
    * Set up Benefit Sessions with frequency/recurrence 
* Review and update Status values (including default Status) on Program Enrollment

Optional



* Configure Benefit Disbursement Field Set if you want to track additional details about a participant

**Prerequisites for End User:**

Required



* Create or confirm Account record for each client 

Optional



* Create Program Enrollment record for each Account
* Group Program Enrollments into Program Cohorts

**Best Practices:**



* Create the Benefit Schedule from the Benefit record.
    * Note: Using the Benefit > New Benefit Schedule button is the only way to create Recurrence Schedule records. The Benefit also needs to be active to be assigned. 
* Establish consistent eligibility processes including where which Salesforce record(s) will store information. . 
* Establish clear check-in and attendance processes including where which Salesforce record(s) will store information.

**How to enter data (recommended):**



* To add participant to all Benefit Sessions for a specific Benefit Schedule, use Benefit Schedule > “Add Participant” button 
    * Can add Account, Contact, or Program Enrollment (if previously created)
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
