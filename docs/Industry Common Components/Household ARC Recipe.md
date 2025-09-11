---
layout: default
title: Household ARC Recipe
nav_order: 1
parent: Actionable Relationship Center (ARC) Graphs
---
# Household ARC Recipe

This recipe shows how you can model households using the Actionable Relationship Center (ARC) in Salesforce.


## Defining a Household

Before building ARC diagrams, agree on what “household” means for your organization. Common definitions include:
* **By residence** – individuals living under the same roof


* **By family ties** – individuals connected by familial relationships, regardless of address
Your choice should reflect how you plan to:



* Report on giving (e.g., household giving summaries)


* Track and deliver programs that involve families or groups

## ARC Visualization

Data assumptions in this example:


* Each individual is assigned to **one** **household only**, to prevent donor giving summaries from double-counting donations

* If needed, relationships between multiple households (e.g., separated households) can be tracked using an **Account-Account Relationship** (not pictured in this diagram)

<img width="700" height="auto" alt="HH ARC Img1" src="https://github.com/user-attachments/assets/6f00fa23-4ea4-4169-8daa-31448ed42b31" />
<br>
<br>

**Note:**  The fields shown in each card are for illustration only to help explain the data model. You can replace them with fields relevant to your use case.

<u>In the Account-Contact Relationship:</u>

1. **Role** is always ‘Household Member’

2. **Primary** **Member** identifies the head of the household

<u>In the Contact-Contact Relationship:</u>

3. **Related** **Role** **Name** identifies the relationship Sonny has with Joshua

## Data model

### Example 1: Household Data Model (pictured in ARC visualization)

This diagram illustrates the records that exist behind the ARC diagram above.


* **Party Relationship Group:** Extension object (not shown in ARC diagram) used to track additional demographic, structural, and operational details about a household or group

* **Business Account:** the household entity

* **Person Accounts:** the individuals

* **Account-Contact Relationships:** the household members

* **Contact-Contact Relationships** how individuals are related, such as spouse, parent, child or sibling

<img width="700" height="auto" alt="HH ARC Img2" src="https://github.com/user-attachments/assets/0d32fd10-9c1a-4069-9136-87a637995e14" />
<br>
<br>

### Example 2: Separated Household Data Model (not pictured in ARC visualization)

For situations where the parents are separated/divorced, a few modifications are required:


* A new Household Account is created for the parent leaving the original household
    * A new Party Relationship Group is created for the new household
    * The corresponding Account Contact Relationship between the parent leaving and the original household must be deleted, as this will affect DPE roll-ups on the household account if kept (i.e., the Active checkbox on the ACR record does not impact the rollup calculation)

* The Active checkbox on the Contact-Contact Relationship between the parents is set to false (Inactive) 

* The Account Contact Relationships for the children leaving the household (Daisy & Dahlia) must be deleted from the original household (Flower Household)
    * New Account Contact Relationships are created between the children and the new household (Sprout Household)
    * 
<img width="700" height="auto" alt="HH ARC Img3" src="https://github.com/user-attachments/assets/ebd7c95d-703d-4c9c-99a7-8713f6b43156" />
<br>
<br>
<br>
## ARC Configuration
