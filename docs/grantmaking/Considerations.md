---
layout: default
title: Considerations
nav_order: 3
parent: Grantmaking
---

# Grantmaking Considerations Overview


## Grantmaking vs. managing grants as a grant seeker:



* Organizations can be both grantmakers and grant seekers, but Agentforce Nonprofit (AFNP) Grantmaking (FKA NPC Grantmaking) is specifically geared towards organizational funders who make charitable grants (and/or PRI loans) to nonprofits.
    * Grantmaking: Organization that implements grant programs and provides funding to individuals/organizations. 
        * AFNP Grantmaking provides additional functionality that supports the various stages of grantmaking activities from inquiry through disbursement and reporting. 
    * Grant seeking: Organizations/individuals looking to apply and receive funds to support their work. 
        * AFNP Fundraising features support grant seeking activities and can be customized to align with the specific needs of how an organization tracks institutional donations and monitoring outcomes of program delivery. 


## Difference between Grantmaking and standard Agentforce Nonprofit (AFNP fka Nonprofit Cloud/NPC)



* Salesforce Pricing Comparison table [here](https://www.salesforce.com/nonprofit/grantmaking-pricing/). 
* Grantmaking licenses include access to Experience Cloud 
    * For each purchased license, the org gets 100 monthly login licenses for the experience portal (Technical Note: This utilizes customer community login license types)
    * Experience portal template to get started with an online grants portal quickly
    * Permissions that enable access to applications, awards, disbursements, outcome tracking and budget expenditure for external portal users within the grants portal, in addition to access for internal staff users
* Grantmaking licenses do not quality for the P10 donated licenses
* Grantmaking enables specific objects, permissions and functionality to control your grantmaking processes. See [data model](https://developer.salesforce.com/docs/atlas.en-us.nonprofit_cloud.meta/nonprofit_cloud/npc_grant_budget_data_model.htm).
* All users who need to see grantmaking specific data must have a paid license.
* Grantmaking (core) vs. Outbound Funds (managed) vs. Grants Management (managed): See comparison [here](https://sfdo-community-sprints.github.io/npc-best-practices/npsp-to-npc-translations/Grantmaking/).
* Grantmaking leverages objects that overlap with other functionality available in AFNP (and even other core industry functionality and common components). Closely monitor each release to ensure updates align with any customizations.


## Trial Orgs vs. Your Purchased Grantmaking Org



* What gets shown during demos and what settings and customizations exist when you start a trial org is not what is available in your new org out-of-the-box when you actually get provisioned one by your AE.
* This means that customizations you saw during a demo is not standard functionality, and functionality will require customization (preferably by working with a consultant partner) to function in the way you run your grants processes.


## Tracking Data with Standard AFNP Grantmaking



* Application and Award tracking - Grantmaking has a two-object model where application data is tracked in a wholly separate object than the award data. 
    * There is no out-of-the-box automation to create an award record or copy the data from the application record as this can be customized to your specific way of working.
    * Disbursements (payments) and ongoing reporting (requirements) are tracked on the grant award only. There is an out-of-the-box automation to schedule out disbursements and requirements for any grant awards - individually or in a batch.
