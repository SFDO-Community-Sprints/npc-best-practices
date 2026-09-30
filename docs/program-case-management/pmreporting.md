---
layout: default
title: Program Management Reports Package
nav_order: 3
parent: Program and Case Management
---

## **Overview** - [Production](https://login.salesforce.com/packaging/installPackage.apexp?p0=04tg7000000TEij) | [Sandbox](https://test.salesforce.com/packaging/installPackage.apexp?p0=04tg7000000TEij)

This is a package of basic reports and custom report types commonly used for tracking Program Management participants and performance in a Salesforce org with Nonprofit Cloud.



* Who should be installing this: System Admins
* Where should this be installed: Follow best practice and install in a sandbox first to test and evaluate. If available, a full sandbox is ideal, but you’ll want one with at least some donation data so you can see report results. When ready, you can deploy to or install directly in production.
* Purpose: To help nonprofits using Nonprofit Cloud for fundraising get started running analysis of their donors and donation history. These reports are a baseline from which additional variations and filters can be added based on business use-cases and needs.


### **Program Management Reporting Requirements**

Pre-installation Requirements: Standard Nonprofit Cloud Program Management features enabled

Before installing this package, you will need to ensure the following:



* Complete all setup steps per [Salesforce documentation](https://help.salesforce.com/s/articleView?id=sfdo.npc_set_up_nonprofit_cloud_parent.htm&type=5) for person accounts, and Program Management settings, and Data Processing Engine.
* You have followed documentation to enable and configure all Program Management features in Agentforce Nonprofit.
* You will use several pieces of the standard Program Management data model, including Person Accounts, Programs, Program Enrollment, Benefits and Benefit Types, Benefit Assignments, Benefit Schedules, Benefit Sessions, etc. 
* You will use Program Management in the way it is prescribed in the documentation.
* You do not already have a “Programs” reports folder. If you do, ensure you select “Rename conflicting components in package” at the top of the install page for “What if existing component names conflict with ones in this package?”.


### **Technical Install Requirements**

To successfully install this package, you will need:



* User Permissions: System Administrator
* Salesforce Instance: Nonprofit Cloud licenses
* Enabled: Person Accounts
* Toggle on: Program and Case Management
* Confirmed: no preexisting “Programs” reports folder or select “Rename conflicting components in package” during install


### **Post-installation Notes**



* The reports contained in the package use core fields that come without any customization. You will most likely customize these to match your business use-cases. For example, you might want to add your own custom fields or sort, group and filter the data differently based on your organization’s defined giving levels.
* Note that reports for Program Cohorts and Case Referrals will be included in later packages so you are not forced to enable those features to use this reporting pack.
* Pay close attention to the report types being referenced. If you choose not to use certain aspects of the Program Management data model, not all of the reports will display the correct data.
* There is one with/without report type included - Benefit Assignments Deluxe. This is to enable inclusion of the Benefit Schedule, Benefit Session, and Benefit Disbursement objects in this report type.


### **Additional Considerations**

This package contains reports focused primarily on Program Management, using the following data objects:



* Person Accounts
* Business Accounts
* Programs
* Program Enrollments
* Benefits
* Benefit Assignments
* Benefit Disbursements
* Benefit Schedules
* Benefit Schedule Assignments
* Benefit Sessions
* Benefit Types
* Units of Measure


## **Program Cohorts Supplemental Reports** - [Production](https://login.salesforce.com/packaging/installPackage.apexp?p0=04tg7000000UV3B) | [Sandbox](https://test.salesforce.com/packaging/installPackage.apexp?p0=04tg7000000UV3B)

This is a package of 3 Program Cohort reports and a custom report type. 


### **Technical Install Requirements**

To successfully install this package, you will need:


* User Permissions: System Administrator
* Salesforce Instance: Nonprofit Cloud licenses
* Enabled: Person Accounts
* Toggle on: Program and Case Management
* Toggle on: Create and manage program cohorts under Program and Benefit Management Settings
* Confirmed: no preexisting “Program Cohorts” reports folder or select “Rename conflicting components in package” during install

This supplemental package contains reports focused on Program Cohorts, using the following data objects:

* Program Cohorts
*	Program
