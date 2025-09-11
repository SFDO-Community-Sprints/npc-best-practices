---
layout: default
title: Individual Fundraising ARC Recipe
nav_order: 2
parent: Actionable Relationship Center (ARC) Graphs
---
# Individual Fundraising ARC Recipe

This recipe shows how you can model Fundraising from an Individual using the Actionable Relationship Center (ARC) in Salesforce.

## ARC Visualization

<img width="700" height="auto" alt="Ind ARC 1" src="https://github.com/user-attachments/assets/10630cda-d2bc-431e-9b5a-2d80177b9540" />
<br>
<br>
<img width="700" height="auto" alt="Ind ARC 2" src="https://github.com/user-attachments/assets/01f055ad-4f2b-4319-a953-e63f17604249" />
<br>
<br>

## Data model
### Example 1: Individual Major Gift
This diagram illustrates the records that exist behind the ARC diagram above.

<img width="700" height="auto" alt="Ind ARC 3" src="https://github.com/user-attachments/assets/7cea654d-34e7-4bfc-bda9-a051b7c08a38" />
<br>
<br>

## ARC Configuration

To only show Recurring Donations and not all Gift Commitments, an **Opportunity Exists** checkbox formula field was built. Gift Commitments are filtered out if from the Recurring Donation component if there is an Opportunity.

<img width="700" height="auto" alt="Ind ARC 4" src="https://github.com/user-attachments/assets/f4a2fe8d-6376-43cc-b186-e8b7301d289f" />
