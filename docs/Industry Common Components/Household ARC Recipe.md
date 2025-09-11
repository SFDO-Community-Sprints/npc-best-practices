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

## ARC Configuration

This ARC will contain 3 elements: the Household (Business Account), Household Member (Person Accounts) and Relationships (Contact Contact Relationships).

Setting the Graph Type to Horizontal Hierarchy will allow for easier viewing.  

<img width="700" height="auto" alt="HH ARC Config 1" src="https://github.com/user-attachments/assets/1e00a7d2-dfeb-45e9-a213-1066c877686f" />
<br>
<br>

Select Account as the first element since you will be viewing this ARC graph from the Household Account record. 

<img width="700" height="auto" alt="HH ARC Config 2" src="https://github.com/user-attachments/assets/a75a256a-5fbf-4abd-aa79-c72d9afc1f98" />
<br>
<br>

The second element adds the Person Accounts related to the Household Account via Account Contact Relationship.

<img width="700" height="auto" alt="HH ARC Config 3" src="https://github.com/user-attachments/assets/b217ae49-7e12-437d-b0ba-0c0b7d4ea9f8" />
<br>
<br>

There is an additional step for this element on the Display tab to set a Custom Label, as well as selecting the fields to display.
<br>
The fields selected to display in this recipe are: 

1. Junction Object.Roles

2. Junction Object.Primary member

<img width="700" height="auto" alt="HH ARC Config 4" src="https://github.com/user-attachments/assets/7b078f57-1b5c-4089-b2be-26bada9c4119" />
<br>
<br>

The third element adds the detailed relationships between the Person Accounts in the household via Contact Contact Relationship.

<img width="700" height="auto" alt="HH ARC Config 5" src="https://github.com/user-attachments/assets/200fc939-23f4-4b5a-ae77-4930bf50a85d" />
<br>
<br>

There is an additional step for this element on the Display tab to set a Custom Label, as well as selecting the fields to display. 
<br>
The fields selected to display in this recipe are: 

1. Junction Object.Party Role Relationship.Related Role Name

<img width="700" height="auto" alt="HH ARC Config 6" src="https://github.com/user-attachments/assets/d6c9b227-d6f3-4c82-ab45-bc32fa8e03cb" />
<br>

