---
layout: default
title: Fundraising Reporting
nav_order: 3
parent: Fundraising 
---
### **Overview** - [Production](https://login.salesforce.com/packaging/installPackage.apexp?p0=04tHp000001nIwG&isdtp=p1) | [Sandbox](https://test.salesforce.com/packaging/installPackage.apexp?p0=04tHp000001nIwG&isdtp=p1)

This is a package of basic reports and custom report types commonly used for analyzing fundraising performance in a Salesforce org with Agentforce Nonprofit (formerly known as Nonprofit Cloud).

* Who should be installing this: System Admins
* Where should this be installed: Follow best practice and install in a sandbox first to test and evaluate. If available, a full sandbox is ideal, but you'll want one with at least some donation data so you can see report results. When ready, you can deploy to or install directly in production. 
* Purpose: To help nonprofits using Agentforce Nonprofit (fka Nonprofit Cloud) for fundraising get started running analysis of their donors and donation history. These reports are a baseline from which additional variations and filters can be added based on business use-cases and needs.


### **Fundraising Reporting Requirements**

Pre-installation Requirements: Standard Agentforce Nonprofit/Nonprofit Cloud fundraising features enabled

Before installing this package, you will need to ensure the following:



* Complete all setup steps per [Salesforce documentation](https://help.salesforce.com/s/articleView?id=sfdo.npc_set_up_nonprofit_cloud_parent.htm&type=5) for person accounts, households, fundraising settings, and Data Processing Engine.
* You have followed documentation to enable and configure all fundraising features in Agentforce Nonprofit
* You will use all pieces of the standard fundraising data model, including person accounts, Party Group Relationships and Account-Contact Relationships for household tracking, Opportunities, Gift Commitments, Gift Transactions, Gift Designations, Gift Transaction Designations, Gift Tributes, Gift Soft Credits, Donor Gift Summaries, Campaigns, etc.
* You will use fundraising in the way it is prescribed in the documentation such as entering donations via the Gift Entry feature and creating Gift Commitments and Gift Commitment Schedules for major gifts
* You do not already have a "Fundraising" reports folder or ensure you select "Rename conflicting components in package" at the top of the install page for "What if existing component names conflict with ones in this package?"

### Technical Install Requirements:
To successfully install this package, you will need:
* User Permissions: System Administrator
* Salesforce Instance: Agentforce Nonprofit (formerly Nonprofit Cloud) licenses 
* Enabled: Person Accounts 
* Toggle on: Fundraising 
* Confirmed: no preexisting "Fundraising" reports folder or select "Rename conflicting components in package" during install

### Post-installation


* The reports contained in the package use core fields that come without any customization. You will most likely customize these to match your business use-cases (for example, you might want to add your own custom fields or sort, group and filter the data differently based on your organization's defined giving levels).
* Pay close attention to the report types being referenced. If you choose not to use certain aspects of Fundraising data model (not recommended), not all of the reports will display the correct data.
    * Example: If you use custom roll-ups to summarize donation totals directly on the account, these reports will not display your data correctly
    * Example: if you enter recurring gift installments as Gift Transactions without Gift Commitments, the reports may not show you accurate data as they are intended to work with the default configuration.

### Additional Considerations:
This package contains reports focused primarily on fundraising, using the following data objects:


* Person Accounts
* Business Accounts
* Opportunities
* Gift Commitments
* Gift Designations
* Gift Transactions
* Gift Transaction Designations
* Gift Tributes
* Soft Credits
* Donor Gift Summaries
* Party Relationship Groups
* Outreach Source Codes
* Payment Instruments

### Index of what's included:


<table>
  <tr>
   <td><strong>Component Name</strong>
   </td>
   <td><strong>Developer (API) Name</strong>
   </td>
   <td><strong>Type</strong>
   </td>
  </tr>
  <tr>
   <td>Fundraising
   </td>
   <td>Fundraising
   </td>
   <td>Folder
   </td>
  </tr>
  <tr>
   <td>Active Recurring Donations
   </td>
   <td>Active_Recurring_Donations_5NN
   </td>
   <td>Report
   </td>
  </tr>
  <tr>
   <td>All Gift Commitments
   </td>
   <td>All_Gift_Commitments_RFY
   </td>
   <td>Report
   </td>
  </tr>
  <tr>
   <td>All Gift Designations
   </td>
   <td>All_Gift_Designations_xUV
   </td>
   <td>Report
   </td>
  </tr>
  <tr>
   <td>All Individuals
   </td>
   <td>All_Individuals_aOr
   </td>
   <td>Report
   </td>
  </tr>
  <tr>
   <td>All Opportunities
   </td>
   <td>All_Opportunities_QAi
   </td>
   <td>Report
   </td>
  </tr>
  <tr>
   <td>All Payment Fund Allocations
   </td>
   <td>All_Payment_Fund_Allocations_bBn
   </td>
   <td>Report
   </td>
  </tr>
  <tr>
   <td>All Payments for Custom Commitments
   </td>
   <td>All_Payments_for_Custom_Commitments_Y60
   </td>
   <td>Report
   </td>
  </tr>
  <tr>
   <td>All Payments for Recurring Donations
   </td>
   <td>All_Payments_for_Recurring_Donations_HA6
   </td>
   <td>Report
   </td>
  </tr>
  <tr>
   <td>All Recurring Donations
   </td>
   <td>All_Recurring_Donations_xxq
   </td>
   <td>Report
   </td>
  </tr>
  <tr>
   <td>Closed Recurring Donations
   </td>
   <td>Closed_Recurring_Donations_jkv
   </td>
   <td>Report
   </td>
  </tr>
  <tr>
   <td>Donors 2 Years Ago But Not Last/This Yr
   </td>
   <td>Donors_2_Years_Ago_But_Not_LastThis_Yr_RWq
   </td>
   <td>Report
   </td>
  </tr>
  <tr>
   <td>Donors Last Year But Not This Yr LYBUNT
   </td>
   <td>Donors_Last_Year_But_Not_This_Yr_LYBUNT_Wek
   </td>
   <td>Report
   </td>
  </tr>
  <tr>
   <td>Donors Some Year But Not This Yr SYBUNT
   </td>
   <td>Donors_Some_Year_But_Not_This_Yr_SYBUNT_fPI
   </td>
   <td>Report
   </td>
  </tr>
  <tr>
   <td>Failing Recurring Donations
   </td>
   <td>Failing_Recurring_Donations_brT
   </td>
   <td>Report
   </td>
  </tr>
  <tr>
   <td>Giving Summary by Household
   </td>
   <td>Giving_Summary_by_Household_DWd
   </td>
   <td>Report
   </td>
  </tr>
  <tr>
   <td>Giving Summary by Individual
   </td>
   <td>Giving_Summary_by_Individual_YGb
   </td>
   <td>Report
   </td>
  </tr>
  <tr>
   <td>Giving Summary by Organization
   </td>
   <td>Giving_Summary_by_Organization_hzO
   </td>
   <td>Report
   </td>
  </tr>
  <tr>
   <td>Honor and Memorial Payments
   </td>
   <td>Honor_and_Memorial_Payments_xEb
   </td>
   <td>Report
   </td>
  </tr>
  <tr>
   <td>Inactive Recurring Donations
   </td>
   <td>Inactive_Recurring_Donations_Sm5
   </td>
   <td>Report
   </td>
  </tr>
  <tr>
   <td>Lapsed Sustainers
   </td>
   <td>Lapsed_Sustainers_Dd9
   </td>
   <td>Report
   </td>
  </tr>
  <tr>
   <td>Month by Month Donation Comparison
   </td>
   <td>Month_by_Month_Donation_Comparison_0Fc
   </td>
   <td>Report
   </td>
  </tr>
  <tr>
   <td>Opportunities Close Rate by Owner
   </td>
   <td>Opportunities_Close_Rate_by_Owner_XtW
   </td>
   <td>Report
   </td>
  </tr>
  <tr>
   <td>Opportunity Gift Default Designations
   </td>
   <td>Opportunity_Gift_Default_Designations_agr
   </td>
   <td>Report
   </td>
  </tr>
  <tr>
   <td>Opportunity Pipeline
   </td>
   <td>Opportunity_Pipeline_17F
   </td>
   <td>Report
   </td>
  </tr>
  <tr>
   <td>Overdue Payments
   </td>
   <td>Overdue_Payments_poO
   </td>
   <td>Report
   </td>
  </tr>
  <tr>
   <td>Overdue Payments for Custom Commitments
   </td>
   <td>Overdue_Payments_for_Custom_Commitments_IK5
   </td>
   <td>Report
   </td>
  </tr>
  <tr>
   <td>Overdue Payments for Recurring Donations
   </td>
   <td>Overdue_Payments_for_Recurring_Donations_FvN
   </td>
   <td>Report
   </td>
  </tr>
  <tr>
   <td>Paid Payment Fund Allocations
   </td>
   <td>Paid_Payment_Fund_Allocations_LC1
   </td>
   <td>Report
   </td>
  </tr>
  <tr>
   <td>Paid Payments
   </td>
   <td>Paid_Payments_5mt
   </td>
   <td>Report
   </td>
  </tr>
  <tr>
   <td>Paid Payments for Custom Commitments
   </td>
   <td>Paid_Payments_for_Custom_Commitments_8QN
   </td>
   <td>Report
   </td>
  </tr>
  <tr>
   <td>Paid Payments for Opportunities
   </td>
   <td>Paid_Payments_for_Opportunities_wCM
   </td>
   <td>Report
   </td>
  </tr>
  <tr>
   <td>Paid Payments for Recurring Donations
   </td>
   <td>Paid_Payments_for_Recurring_Donations_zKC
   </td>
   <td>Report
   </td>
  </tr>
  <tr>
   <td>Paid Payments from Households
   </td>
   <td>Paid_Payments_from_Households_lfJ
   </td>
   <td>Report
   </td>
  </tr>
  <tr>
   <td>Paid Payments from Individuals
   </td>
   <td>Paid_Payments_from_Individuals_lOr
   </td>
   <td>Report
   </td>
  </tr>
  <tr>
   <td>Paid Payments from Organizations
   </td>
   <td>Paid_Payments_from_Organizations_f1i
   </td>
   <td>Report
   </td>
  </tr>
  <tr>
   <td>Paid Payments without Fund Allocations
   </td>
   <td>Paid_Payments_without_Fund_Allocations_swE
   </td>
   <td>Report
   </td>
  </tr>
  <tr>
   <td>Top 25 All-Time Individual Donors
   </td>
   <td>Top_25_AllTime_Individual_Donors_Fsb
   </td>
   <td>Report
   </td>
  </tr>
  <tr>
   <td>Top 25 Won Opportunities
   </td>
   <td>Top_25_Won_Opportunities_uP9
   </td>
   <td>Report
   </td>
  </tr>
  <tr>
   <td>Unpaid Payments
   </td>
   <td>Unpaid_Payments_7Oa
   </td>
   <td>Report
   </td>
  </tr>
  <tr>
   <td>Unpaid Payments for Custom Commitments
   </td>
   <td>Unpaid_Payments_for_Custom_Commitments_cSU
   </td>
   <td>Report
   </td>
  </tr>
  <tr>
   <td>Unpaid Payments for Recurring Donations
   </td>
   <td>Unpaid_Payments_for_Recurring_Donations_lcw
   </td>
   <td>Report
   </td>
  </tr>
  <tr>
   <td>Donor Gift Summaries (Deluxe)
   </td>
   <td>Donor_Gift_Summaries_Deluxe
   </td>
   <td>Custom Report Type
   </td>
  </tr>
  <tr>
   <td>Donor Gift Summaries + Accounts without Donor Gift Summaries
   </td>
   <td>Donor_Gift_Summaries_Accounts_without_Donor_Gift_Summaries
   </td>
   <td>Custom Report Type
   </td>
  </tr>
  <tr>
   <td>Gift Commitments (Deluxe)
   </td>
   <td>Gift_Commitments_Deluxe
   </td>
   <td>Custom Report Type
   </td>
  </tr>
  <tr>
   <td>Gift Default Designations Related To Opportunities
   </td>
   <td>Gift_Default_Designations_Related_To_Opportunities
   </td>
   <td>Custom Report Type
   </td>
  </tr>
  <tr>
   <td>Gift Designations (Deluxe)
   </td>
   <td>Gift_Designations_Deluxe
   </td>
   <td>Custom Report Type
   </td>
  </tr>
  <tr>
   <td>Gift Transaction Designations (Deluxe)
   </td>
   <td>Gift_Transaction_Designations_Deluxe
   </td>
   <td>Custom Report Type
   </td>
  </tr>
  <tr>
   <td>Gift Transactions (Deluxe)
   </td>
   <td>Gift_Transactions_Deluxe
   </td>
   <td>Custom Report Type
   </td>
  </tr>
  <tr>
   <td>Gift Transactions Related To Accounts
   </td>
   <td>Gift_Transactions_Related_To_Accounts
   </td>
   <td>Custom Report Type
   </td>
  </tr>
  <tr>
   <td>Gift Tributes (Deluxe)
   </td>
   <td>Gift_Tributes_Deluxe
   </td>
   <td>Custom Report Type
   </td>
  </tr>
</table>
