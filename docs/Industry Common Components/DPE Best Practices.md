---
layout: default
title: DPE Best Practices
nav_order: 3
parent: Data Processing Engine
---
# **DPE Best Practices**

**Monthly Limits**



* Each org has a [monthly limit](https://help.salesforce.com/s/articleView?id=ind.dpe_limits.htm&type=5) of DPE processing time, which is 30 hours as of August 2025
* Accounting Subledger (ASL) DPE definitions have hit limits in the past. Weekly runs rather than daily may help your org stay within the monthly limits for the ASL definitions.
* Running most of the other DPE definitions daily usually doesn’t exceed the limit, as the tool is very efficient, but it’s important to monitor consumption in your own org, particularly if you intend to run your DPE definitions more frequently. See the [Monitoring & Troubleshooting section](https://sfdo-community-sprints.github.io/npc-best-practices/Industry%20Common%20Components/Monitoring%20and%20Troubleshooting/).

 
**Best Practices**


* Admins need to clone the standard DPE definition templates and create scheduled flows to run the DPE definitions on a schedule. 
* Salesforce may release updates to the DPE definitions each time there’s a major release. When you clone a particular template, it is a snapshot of the DPE definition from that point in time, and will not be updated with new Salesforce releases. Therefore, some release management is required—you need to clone the most recent DPE definition to get the latest updates.
* The recommended practice is to include the release (e.g., Winter 26) in the name of a cloned DPE definition so you know which version it is. 
* When using DPE, there are two runtime platforms that the DPE definition can run on–CRM Analytics and Data Cloud. Most of the NPC definitions are created using CRM Analytics, with only the CSV Import definition using Data Cloud. In general you will want to select CRM Analytics if you are processing data that is in Salesforce objects (i.e., not in Data Cloud DMO objects or Calculated Insights).
* When creating scheduled flows to automatically update your DPE definitions, it is important to consider timing and sequencing. If separate definitions referencing the same object(s) run at the same time, the runs may fail. Avoid this by scheduling runs at least 15 minutes apart. 
* Consider the sequence of your DPE definition scheduled runs. Are there any dependencies that require a certain definition to run before another?
    * Example: your custom DPE definition relies on updated donation totals, so needs to run after the Donor Gift Summary DPE definition completes
* In multicurrency orgs, the currency of the Writeback User is used for calculations.
* Household accounts need to have a [Party Relationship Group record](https://sfdo-community-sprints.github.io/npc-best-practices/stakeholder-management/stakeholder-management-prerequisites/#householdswhats-different), and individuals need Account-Contact Relationships with the Household Account for the Donor Gift Summary DPE Definition to summarize correctly.

**Maintaining DPE Definitions from Standard Templates**

Salesforce releases periodic updates to the out-of-the-box DPE definitions it provides. 


* To use an updated definition, you need to clone and activate it in the same way you did at implementation. 
* The DPE definitions, particularly the ones for Fundraising, have had regular updates to them released. 
* Before a new Salesforce release is pushed to production, if the release notes indicate a DPE definition that you’re using has been updated, you may need to review your DPE definitions and test them in a sandbox.

After a Salesforce release, you may need to review and test DPE definitions in a sandbox before activating in production. Check the release notes to see if a DPE definition that you’re using has been updated.

Generally, any time you create a new DPE definition, you will need to update the flow action referenced in your schedule triggered flows to make sure they are referencing the most current version of your DPE. 

For the three fundraising DPE definitions, Salesforce has provided a flow template and flow action that will automatically reference the most current version of those three DPE definitions. You can find more detail about the template [here](https://help.salesforce.com/s/articleView?id=sfdo.fundraising_set_up_automatic_updates_for_fundraising_rollups.htm&type=5). 



* Careful consideration is needed before setting up automatic updates.
* This is a process Salesforce has developed to enable admins to automatically keep clones of the base NPC DPE definitions up to date with each release.
* If you choose this process, definitely do NOT customize the cloned DPE definitions—the automatic updates will overwrite any customizations in the cloned DPE definitions.
* All customizations should be in separate DPE definitions, which will be unaffected by the above process.
    * You can trigger multiple DPE definitions in a single Flow (e.g. your Flow can run the cloned DPE definition first, then run any other DPE definitions after).
* You may not want automatic updates without testing first—it’s important to make sure the newly updated definition is compatible with your Salesforce org and produces expected results.
