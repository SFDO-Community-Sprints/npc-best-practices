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

