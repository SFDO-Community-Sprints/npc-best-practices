---
layout: default
title: Person Accounts
nav_order: 1
parent: Decision Guides
---

# Person Accounts
Agentforce Nonprofit documentation generally recommends that Person Accounts are enabled as a part of set up. Salesforce makes one exception in their recommendation to enable Person Accounts. “Grantmaking customers who make the vast majority of their grants to organizations rather than individuals are likely to find the Contact + Business Account model more appropriate than Person Accounts.” ([see rest of note](https://help.salesforce.com/s/articleView?id=sfdo.npc_prerequisites.htm&type=5))  

With this exception, there is a decision grantmakers need to make when implementing Agentforce Nonprofit. Below is a list of questions to consider when making this decision.  

<b>If you answer “yes” to any of the following questions, you most likely need to enable Person Accounts.</b>  

## Does your organisation work with individuals in a funding/tracking/program context? 
This page defines “individuals” as a single human constituent whose interactions and transactions are tracked independently of any employer or business affiliation.  

Examples of an individual would be:
<ul>
    <li>A donor</li>
    <li>A volunteer</li>
    <li>A referral</li>
    <li>A participant</li>
    <li>A person for whom there is a case</li>
    <li>A mentor/mentee</li>
    <li>A person in a cohort</li>
    <li>A student</li>
    <li>A recipient of a disbursement</li>
</ul>

### A few more questions about your work with individuals:  
<b>1. Do you communicate with individuals?</b>  
The communication doesn’t need to be specific to grantmaking, but it can be any sort of communication sent on behalf of your organisation. For example,   
    <ul>
    <li>Community email broadcast</li>
    <li>Newsletters</li>
    </ul>

<b>2. Do you fundraise with individuals?</b>  
If you only solicit funding from organisations and not individual donors, and you don’t require the use of the “fundraising” features, you may not need person accounts.  

However, if there is even a remote possibility that you will use any of the fundraising features, you should consider enabling person accounts to avoid the need to migrate to person accounts in the future.  

As of the first publish date of this page, the following functionality does not work in AFNP Fundraising when person accounts are not enabled: 
    <ul>
    <li>Gift entry grid</li>
    <li>Fundraising agents </li>  
    <li>Address automation (contact point) </li>
    <li>Flexipage components on Person Account Record Page</li>
    <li><b>Note:</b> There also may be future development that is specific to person accounts thus you will need to do additional research when making this decision </li>
    </ul>

## Do you use any other AFNP features OR do you EVER plan to use any other AFNP features (volunteer, programs, fundraising, etc.) in the future? 
Since Person Accounts are required for most AFNP functionality, they should most likely be enabled in an org that has cross-departmental functionality in the same system.  

If you start with not enabling Person Accounts and then find that you add functionality that requires Person Accounts in the future, it will require a migration including a data migration at that time. By enabling Person Accounts at the start, you will avoid the extra time and effort to migrate in the future.  

## Do you want your whole organisation in a single salesforce org (e.g. fundraising, programs management, case management, sales/e-commerce, grantmaking in one place)? 
If fundraising, program management, and grantmaking (or other organisation functions) exist within the same organisation, a single Salesforce org is the right approach. It consolidates financials, enables cross-org analytics, brings all org-specific features under one roof, and provides the flexibility to expand all areas of the organisation and system without the overhead and complexity of managing multiple orgs.  

Since Person Accounts are required for most AFNP functionality, they should most likely be enabled in an org that has cross-departmental functionality in the system.  

