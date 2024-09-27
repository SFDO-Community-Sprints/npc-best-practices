---
title: Stakeholder Management
parent: NPSP to NPC Translations
nav_order: 1
---

# Stakeholder Management

<div align="center">## Householding Comparison</div>div>
| Capability                                          | NPSP                                                        | Nonprofit Cloud                                                                                      |
| --------------------------------------------------- | ----------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- |
| Household record for every contact                  | Yes (for every contact not related to a business account)   | No - only when needed                                                                                |
| How households are modeled                          | Account record type                                         | Business Account record type with related Party Relationship Group record with the type of Household |
| Relationships between individuals                   | Relationship object                                         | Contact Contact Relationship record with related Party Role Relationship                             |
| Relationships between individuals and organizations | Affiliation object for boards, businesses, etc.             | Account Contact Relationship object for boards, businesses, etc.                                     |
| Relationships between individuals and households    | Contact lookup to Account to relate a person to a household | Account Contact Relationship to relate a person to a household                                       |
| Relationships between Non-household groups          | Accounts with affiliations                                  | Account record type with related Party Relationship Group record with the type of Group              |
| Addresses                                           | Address custom object tied to Account                       | Contact Point Address object tied to Account                                                         |
| Household merging                                   | Not supported                                               | Guided wizard to merge and split accounts                                                            |



## Households, Relationships, and Affiliations

| Relationship to Map                            | NPSP                                                | Nonprofit Cloud                                                          |
| ---------------------------------------------- | --------------------------------------------------- | ------------------------------------------------------------------------ |
| Households                                     | Account Record Type                                 | Business Account Record Type with  related Party Relationship Group      |
| Relationship Between Individual and Households | Lookup field on Contact Object to Household Account | Account Contact Relationship Record                                      |
| Relationships Between Individuals              | Relationship Record                                 | Contact Contact Relationship record with related Party Role Relationship |
| Relationships Between Individuals and Accounts | Affiliation Record                                  | Account Contact Relationship Record                                      |
| Relationships Between Accounts                 | N/A                                                 | Account Account Relationship record with related Party Role Relationship |
