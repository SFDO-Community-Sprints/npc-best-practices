---
layout: default
title: Program Use Cases
nav_order: 1
parent: Program and Case Management
has_children: true
---

# Program Management Use Cases
For nonprofits, program data can be collected, tracked, and managed in multiple ways, often requiring different structures and workflows. The Program Management Use Cases outlined here serve as a guide to help nonprofits effectively document and monitor their program activities within Salesforce’s Nonprofit Cloud. 

We acknowledge that each nonprofit operates with unique processes and may require specific customizations to align Salesforce with their programmatic needs. If this is the first time you are setting up Program Management for your org, we recommend working using documentation like the <a href="/npc-best-practices/program-management-mapping-deck.md">Program Management Mapping Deck</a> to determine your program structure in Salesforce.

## **Overall Requirements**

**Prerequisites for Salesforce Admin:**



* Required
    * NPC Program Management setup must be completed
        * Person Accounts must be configured
        * Basic setup including permission set assignments
* Optional
    * Review Lightning Record pages and remove unneeded components
    * Setup and configure Data Processing Engine
    * Add a custom rollup summary field to count the number of Benefit Sessions for a Benefit Schedule
    * Turn on Program Cohort creation if your organization tracks participants by predefined group 

**Prerequisites for End User:**



* Required
    * Create Program records
    * Create Unit of Measure records
    * Create Benefit Type records
    * Create Benefit records
* Optional
    * Create Goal Definition records
    * Create Program Cohort records
