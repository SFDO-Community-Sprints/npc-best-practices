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
