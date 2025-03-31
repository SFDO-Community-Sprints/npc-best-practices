---
title: Templates & Packages
parent: Stakeholder Management
nav_order: 2
---
# Templates & Packages

For issues with items on this page, please email <npcbestpractices@gmail.com>

## Templates
### Party Role Relationships Import Template - [Template Download](https://docs.google.com/spreadsheets/d/1wIwShGKk2uE3T8Eyn7rHp9KcO0NvK2-Kb5bdeZvhG0Q/edit?usp=sharing)
* See the [Stakeholder Management Prerequisites](https://sfdo-community-sprints.github.io/npc-best-practices/stakeholder-management/stakeholder-management-prerequisites/#configure-party-role-relationships) page for details


## Packages
### Relationships Unmanaged Package - [Production](https://login.salesforce.com/packaging/installPackage.apexp?p0=04tHp000001nIDE) | [Sandbox](https://test.salesforce.com/packaging/installPackage.apexp?p0=04tHp000001nIDE)

This package provides Flows to simplify the creation of Relationship records, including Contact-Contact, Account-Contact, and Account-Account Relationships. It also ensures inverse relationships are managed automatically, deleting them when the corresponding Relationship is removed. Additionally, the package includes a Flow to automatically convert newly created Contacts into Person Accounts. Custom Report Types and sample Reports are included to support various relationship types within Nonprofit Cloud. This package is also compatible with Education Cloud.

![Screenshot 2025-03-31 at 3 24 49 PM](https://github.com/user-attachments/assets/ad0b7c19-ad25-437e-8651-3c7a45ef6e82)


**Pre-installation Requirements**
* Enable Person Accounts
* Enable Contacts to Multiple Accounts
* Enable Group Membership
    * Search for 'Group Membership Settings' in Setup - NOT the one under Financial Services, the one under Group Membership
* Assign Permission Set
    * Group Membership

*Much of this is covered under the [Set up Nonprofit Cloud](https://help.salesforce.com/s/articleView?id=sfdo.npc_set_up_nonprofit_cloud.htm&type=5) documentation steps.*


**Post-installation**
* Make sure to check that your Person Account and Business Account record type developer names match, otherwise you may need to update the 'Convert Contact to Person Account' flow:
    * PersonAccount
    * Business_Account
* If you would like to share the sample reports with non-admin users, navigate to the Report Folder ‘Relationships’ to share with additional users.
* Create a New Action on the Account Object, that calls the ‘Create a Relationship Flow’.  *The Create a Relationship Guided Flow is a single flow that calls sub-flows depending on which type of relationship the user is creating.
 ![Screenshot 2025-03-31 at 3 21 41 PM](https://github.com/user-attachments/assets/abf67022-204b-4a1a-92e8-8683c51ea8da)

 Add the Action to your Account page layouts and/or Account Lightning pages.


