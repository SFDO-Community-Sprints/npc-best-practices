---
layout: default
title: Walk-In Program Participation (Predefined Sessions)
nav_order: 2
parent: Program Use Cases
---

# Walk-In Program Participation (Predefined Sessions)
**Definition:**

Tracking people who receive a service or benefit as part of a previously created program without completing a pre-registration process. The program has predefined dates and start/end times. Participants arrive as needed, provide some basic information, and attendance is tracked. May be part of the core mission or related to the mission. May be outcome-associated or not. Works well for organizations that have membership or other ways in which Account records are created before the program. 

**Examples:**



* An education nonprofit offers drop-in support, where students sign in with their name and school upon arrival.
* A senior center holds weekly exercise classes for members who can attend as they choose.
* A community center provides a weekly meal program, tracking attendee names and postal codes for repeat participation.

**Prerequisites for Salesforce Admin:**

Required



* Overall requirements met
* Set up program specific information
    * Set up Benefit Schedules with start/end dates and times
    * Set up Benefit Sessions with frequency/recurrence 

**Prerequisites for End User:**

Required



* Create or confirm Account or Person Account records for each client

**Best Practices:**



* Keep required fields on Account and Person Account records low to reduce time and complexity when creating these records on the spot. 

**How to enter data (recommended):**



* Add participant to the Benefit Session > “Add Participant” button and update Disbursement Status.
    * Creates Benefit Assignment and Benefit Disbursement records with default Disbursement Status and Program Enrollment record if not already created
    * Update Disbursement Status once attendance is complete

**How to enter data (other options):**



* Record creation via Salesforce automation (screen flows, OmniStudio)
* Record creation via third-party form tool
* Record creation via data import tool
    * NOTE: The Data Import Wizard does not work with Nonprofit Cloud objects.


