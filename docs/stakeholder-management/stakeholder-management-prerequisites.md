---
title: Stakeholder Management Prerequisites
parent: Stakeholder Management
nav_order: 1
---
# Stakeholder Management Prerequisites

## Configure Person Accounts

In Nonprofit Cloud, Person Accounts track individual stakeholders, such as donors, volunteers, program participants, or board members. They combine fields from the Account and Contact objects and display them as one record.

**To configure Person Accounts, review the following resources:**

[Enable Person Accounts per the NPC Setup Basics](https://help.salesforce.com/s/articleView?id=sfdo.npc_set_up_nonprofit_cloud.htm&type=5)

[Trailhead: Stakeholder Management in Nonprofit Cloud](https://trailhead.salesforce.com/content/learn/modules/stakeholder-management-in-nonprofit-cloud)

**Additional Considerations**:

**Can Person Accounts coexist with Contacts in my Salesforce org?**



* Yes, but be aware that some functionality in Nonprofit Cloud is dependent on Person Accounts and future functionality may rely on it as well since it is the recommended account-contact model for NPC.

**What is the best practice for building fields? Do I build on the Account object or Contact Object?**



* Contact-specific information should be built on the Contact Object (e.g. Birthdate, Ethnicity, Demographics). This is especially important for integrated apps like marketing automations that may look at Contact for fields even though they work with Person Accounts.
* Account-specific information should be built on the Account Object

**What if a field applies to both Accounts and Contacts?**



* This will be a case by case decision. Evaluate the presence of integrations, etc. when deciding
    * Example: I have a checkbox for VIP that I use for both business and person accounts. 


## Households--What’s Different?

In NPSP, every Contact record is associated with a household account. NPC provides a flexible model allowing customers to choose whether to use households. Organizations not needing to group contacts by household can use Person Accounts directly, bypassing the need to create a household Account record. Conversely, for those requiring household grouping, the Party Relationship Group Wizard simplifies this process. Ultimately, households are optional, and their creation should be based on specific needs.

For NPC, households are a four record model:



* **Account** Record that represents the household with a Business Account record type
* **Person Account** Record that represents the household member.
* **Account Contact Relationship** Record that relates the Person Account to the household Business Account record.
* **Party Relationship Group** Record that indicates this Business Account is a Household (extension object that is necessary for backend system functionality)

To create a household in NPC, use the following steps:



1.    Create all household members as Person Accounts.
2.    Navigate to the Party Relationship Group Tab, and Click “New Group”. Add the related Person Accounts as members of the group then click Next.
3.    Optional: Follow the next page of the wizard to complete the creation of Contact-Contact Relationships between each of the members of the household.

The New Group wizard will create the Business Account for the household as well as the Account Contact Relationships to relate each person you added to that household account.

Considerations 



* Don’t skip the creation of Party Relationship Group records if designing a custom flow for households. It is critical for some areas of NPC household functionality, particularly in Fundraising.


## Configure Party Role Relationships

Party Role Relationships refer to the associations between different parties (such as contacts and accounts) within Salesforce.

For example, in a Social Service Agency, the Case Manager will need to track the relationships that exist between their clients, family members, and other agencies their client might work with. 

In NPSP, the Relationship object was used to create reciprocal relationships between People (e.g. Parent and Child, or Husband and Wife). The values for Relationship roles came pre-configured.

In NPC, the client has the flexibility to configure only the Party Relationship Roles that they need. Download a copy of the [Party Relationship Roles data import template](https://docs.google.com/spreadsheets/d/1wIwShGKk2uE3T8Eyn7rHp9KcO0NvK2-Kb5bdeZvhG0Q/edit?usp=sharing) to begin configuring the roles you will need in your organization. The first tab of the spreadsheet is a short list of common relationships to get you started. The second tab is an expanded list of common possible roles that you may be interested in. Use whiehver tab is best for your organization and alter as needed. 

**Do I need to configure Party Role Relationships?**



* Not necessarily.  These only need to be created if you want to relate a person to another person, or a person, or a Busines or Organization to another Business or Organization.
