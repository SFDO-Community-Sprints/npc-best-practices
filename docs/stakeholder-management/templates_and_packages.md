---
title: Templates & Packages
parent: Stakeholder Management
nav_order: 3
---
# Templates & Packages

For issues with items on this page, please email <npcbestpractices@gmail.com>

## Templates
### Party Role Relationships Import Template - [Template Download](https://docs.google.com/spreadsheets/d/1wIwShGKk2uE3T8Eyn7rHp9KcO0NvK2-Kb5bdeZvhG0Q/edit?usp=sharing)
* See the [Stakeholder Management Prerequisites](https://sfdo-community-sprints.github.io/npc-best-practices/stakeholder-management/stakeholder-management-prerequisites/#configure-party-role-relationships) page for details


## Packages
### Relationships Unmanaged Package - [Production](https://login.salesforce.com/packaging/installPackage.apexp?p0=04tHp000001n72t) | [Sandbox](https://test.salesforce.com/packaging/installPackage.apexp?p0=04tHp000001n72t)

This package includes Flows to streamline the creation of Relationship records (Contact Contact Relationship, Account Contact Relationship, Account Account Relationship) including their inverse relationships, as well as a Flow to automatically convert created Contacts to Person Accounts. It also includes Custom Report Types and sample Reports for the various relationship types used in Nonprofit Cloud. This package also works for Education Cloud.

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
