---
layout: default
title: Data Processing Engine
nav_order: 1
parent: Industry Common Components
---
# Data Processing Engine

Audience: Salesforce admins at nonprofits and consulting partners

Goal: Enable someone to get started with Data Processing Engine.

- [Overview](https://sfdo-community-sprints.github.io/npc-best-practices/Industry%20Common%20Components/Data%20Processing%20Engine/#what-is-data-processing-engine)
- [Users & Permissions](https://sfdo-community-sprints.github.io/npc-best-practices/Industry%20Common%20Components/Data%20Processing%20Engine/#users-and-permissions)
- [Setup Steps for Standard DPE Definitions](https://sfdo-community-sprints.github.io/npc-best-practices/Industry%20Common%20Components/Data%20Processing%20Engine/#setup-steps-for-standard-dpe-definitions) 
- [DPE Best Practices](https://sfdo-community-sprints.github.io/npc-best-practices/Industry%20Common%20Components/Data%20Processing%20Engine/#dpe-best-practices)
- [Monitoring and Troubleshooting](https://sfdo-community-sprints.github.io/npc-best-practices/Industry%20Common%20Components/Data%20Processing%20Engine/#monitoring--troubleshooting)

### What is Data Processing Engine?

Data Processing Engine (DPE) is a declarative feature available with the new Nonprofit Cloud (as well as some other industry clouds) to process and manipulate large volumes of data efficiently. It uses configuration-based rules and flows to handle very large volumes of data that might cause timeouts with, say, Apex-based calculations. Calculations are offloaded for processing to either the CRM Analytics or Data Cloud platforms, depending on the configuration you choose. The results are then used to update your Salesforce records.

For nonprofits, DPE is used to make calculations about donors and donations; program participation and service delivery; and Accounting Subledger transactions.

As you dive into DPE, it can get complex very quickly—don’t panic! You can set up the standard DPE definitions with general admin skills, and we have resources to help you get started. 

### When and where DPE is used in NPC

Several DPE definition templates are provided out-of-the-box with NPC. We recommend using these templates. They are relatively easy to set up and provide very helpful summary information for users. Note that some templates may not be visible until you enable the corresponding feature set, such as Fundraising. Currently, all the out-of-the-box Nonprofit Cloud DPE definitions use CRM Analytics for processing. 

Fundraising DPE Templates:



* [DonorGiftSummary](https://help.salesforce.com/s/articleView?id=sfdo.fundraising_track_gift_donor_trends_rollups.htm&type=5)
* [GiftDesignation](https://help.salesforce.com/s/articleView?id=sfdo.fundraising_track_gift_donor_trends_rollups.htm&type=5)
* [OutreachSummary](https://help.salesforce.com/s/articleView?id=sfdo.fundraising_track_outreach_trends_with_rollups.htm&type=5)
* [Fundraising Account Actionable List Template ](https://trailhead.salesforce.com/content/learn/projects/fundraising-portfolios-with-actionable-lists) 
    * Help documentation for this one is not nonprofit-specific: [Creating Actionable Lists by Using Actionable Segmentation](https://help.salesforce.com/s/articleView?id=sf.actionable_segmentation.htm&type=5) 

Program and Benefit Management DPE Templates:



* [Aggregate Benefit Assignment and Benefit Disbursement](https://help.salesforce.com/s/articleView?id=ind.prog_case_mgmt_prog_mgmt_summary_calc.htm&type=5)
* [Aggregate Program Enrollment](https://help.salesforce.com/s/articleView?id=ind.prog_case_mgmt_prog_mgmt_summary_calc.htm&type=5)

Accounting Subledger DPE Templates:



* [Accounting Subledger Processes](https://help.salesforce.com/s/articleView?id=sfdo.asl_jobs.htm&type=5)

### DPE Help Articles



* [Data Processing Engine](https://help.salesforce.com/s/articleView?id=ind.dpe_intro.htm&type=5)
    * [Node types and how to use them](https://help.salesforce.com/s/articleView?id=ind.dpe_nodes.htm&type=5)
    * [Aggregate functions and how to use them](https://help.salesforce.com/s/articleView?id=ind.dpe_group_aggregate.htm&type=5)
* [Data Processing Engine Definitions](https://help.salesforce.com/s/articleView?id=xcloud.data_processing_engine_jobs.htm&type=5)
* [Configure Data Processing Engine Components](https://help.salesforce.com/s/articleView?id=ind.energy_pcm_configure_data_processing_engine_components.htm&type=5)
* [Use Data Processing Engine Templates](https://help.salesforce.com/s/articleView?id=ind.insurance_clone_data_processing_engine_templates.htm&type=5)
* [Automate Data Processing Engine Definition to run using Salesforce Flows](https://help.salesforce.com/s/articleView?id=ind.dpe_run.htm&type=5)
* NPC Trailheads: 
    * [Data Processing Engine Basics](https://trailhead.salesforce.com/content/learn/modules/data-processing-engine-basics)
 
### **Users and Permissions**

 \
The key permissions for enabling and configuring Data Processing Engine are in the **Data Pipelines Base User** permission set. This permission set is associated with a permission set license, of which only 3 are included as standard with NPC. Therefore, this permission set needs to be assigned judiciously. 

If you are not using fundraising, just assign the Data Pipelines Base User permission set directly to the users who need it. (It is not included in any other standard permission set groups.)

If you are using fundraising, note that the Data Pipelines Base User permission set is included in the standard Fundraising Admin permission set group. Therefore, if you have multiple admins, you need to assign the permission set directly to only the users who need it, and create a custom permission set group that doesn’t include Data Pipelines Base User for other admins. 

Users who only need to see the results of DPE calculations just need read access to the appropriate objects and fields.

Additional permission sets are needed if you are using the flexcards to display Program Management DPE results, or [Fundraising Portfolios with Actionable Lists](https://trailhead.salesforce.com/content/learn/projects/fundraising-portfolios-with-actionable-lists?trailmix_creator_id=strailhead&trailmix_slug=prepare-for-your-salesforce-nonprofit-cloud-consultant-npc-cred).



* Program management users need the OmniStudio User permission set if flexcards are in use.
    * [Security and Permissions for Nonprofit Cloud](https://help.salesforce.com/s/articleView?id=sfdo.npc_nonprofit_cloud_permission_sets.htm&type=5)
* Actionable Segmentation users need the Query for Data Pipelines User permission set. 
    * [Actionable Segmentation Basics](https://help.salesforce.com/s/articleView?id=ind.actionable_segmentation_basics.htm&type=5)
    * [Assign Permission Sets for Actionable Segmentation](https://help.salesforce.com/s/articleView?id=ind.actionable_segmentation_assign_permissions.htm&type=5)

**Relevant Users for Basic Setup**



* **System Administrator**: needs the Data Pipeline Base User permission set assigned
* **Integration User** (assigned the Analytics Cloud Integration User profile): needs at least Read access to every object and field referenced in DPE definitions. Assign the object/field permissions directly to the Analytics Cloud Integration User profile  - you do **NOT** need to assign a Fundraising Access permission set license to the Integration User.
* **Writeback User:** needs full CRED access to all objects and fields referenced in the definition
    * This is the user that the DPE uses to create and update records, and is specified in the Writeback nodes of the definition
    * Must have permissions to create/read/edit/delete
    * Note that the Writeback User defaults to the Default Workflow User ([set in Process Automation Settings](https://help.salesforce.com/s/articleView?id=platform.workflow_defaultuser.htm&type=5)), but does not have to be the same user.

### **Setup Steps for Standard DPE Definitions**

These instructions assume you have already [enabled the NPC feature areas](https://help.salesforce.com/s/articleView?id=sfdo.npc_enable_and_configure_nonprofit_cloud_features.htm&type=5) you will be using, such as Fundraising or Program and Benefit Management.



1. Assign permission set to System Admin user:
   - a. Data Pipelines Base User (see note above)
2. Specify a Default Workflow User in Setup → Process Automation Settings
   - a. If this user is also the Writeback user, the user will need to have full CRED access to data that is updated in the Writeback nodes 
3. If the Writeback User is **not** the same as the Default Workflow User, assign Data Pipelines Base User permission set to the Writeback User
   - a. Writeback user defaults to the Default Workflow User but this can be overridden
4. The Integration User (the one assigned the [Analytics Cloud Integration User profile](https://help.salesforce.com/s/articleView?id=analytics.bi_templates_field_level_security.htm&type=5)) should have at least Read access to data that is aggregated by DPE 
   - a. You may need to update the Analytics Cloud Integration User profile or create a permission set to grant access to some of the standard NPC objects (for example, Gift Transaction for fundraising)
5. Enable Data Pipelines ⇒ From Setup → Data Pipeline → Enable [toggle right] → Under “Enable output connectors” → Select “Salesforce” → it will auto-save.
6. To clone and activate[ DPE definition](https://trailhead.salesforce.com/content/learn/projects/create-fundraising-rollups-with-data-processing-engine/prepare-for-your-new-rollups) templates:
   - a. Go to Setup → Data Processing Engine
   - b. Click on a DPE definition (for example, “Outreach Summary”) to open it
   - c. Select Save As. Give it a name that distinguishes it from the template and preferably includes the current Salesforce release (e.g., Winter 26)
   - d. Click Activate in the new definition you just created
7. [Create scheduled flows](https://trailhead.salesforce.com/content/learn/projects/create-fundraising-rollups-with-data-processing-engine/prepare-for-your-new-rollups) to run the DPE definition(s) nightly
   - a. For DPE definitions with date inputs, such as the Donor Gift Summary, you need to create formulas or constants to use as inputs to the flow action, rather than entering literal dates
   - b. If you want to run a DPE definition immediately, you can open it and click Run Definition
8. Update record pages to display results as follows:
   - a. **Donor Gift Summary**: configure the Related Record Detail Display component on the Account page
   - b. **Outreach Summary**: configure the Related Record Detail Display component on the Campaign page
   - c. **Gift Designation**: these totals are saved directly on the Gift Designation record, so the Related Record Detail Display is not needed for this case. Just organize the fields on the record page as you want.
   - d. **Aggregate Program Enrollment**: Updates fields on the program record. There is also a flex card that can be added to the Program page layout.
   - e. **Aggregate Benefit Disbursement and Benefit Assignment**: Updates fields on Benefit and Program Enrollment records. There is also a flex card that can be added to the page layouts. \


For a step-by-step run-through of steps 6 & 7 see [Prepare for Your New Rollups ](https://trailhead.salesforce.com/content/learn/projects/create-fundraising-rollups-with-data-processing-engine/prepare-for-your-new-rollups)on Trailhead.
### **DPE Best Practices**

**Monthly Limits**



* Each org has a [monthly limit](https://help.salesforce.com/s/articleView?id=ind.dpe_limits.htm&type=5) of DPE processing time, which is 30 hours as of August 2025
* Accounting Subledger DPE definitions have hit limits in the past. Weekly runs rather than daily may help your org stay within the monthly limits.
* Running most of the other DPE definitions daily usually doesn’t exceed the limit, as the tool is very efficient, but it’s important to monitor consumption in your own org, particularly if you intend to run your DPE definitions more frequently. See the Monitoring & Troubleshooting section [add link when building Github page]

 \
**Best Practices**



* Admins need to clone the standard DPE definition templates and create scheduled flows to run the DPE definitions on a schedule. 
* Salesforce may release updates to the DPE definitions each time there’s a major release. When you clone a particular template, it is a snapshot of the DPE definition from that point in time, and will not be updated with new Salesforce releases. Therefore, some release management is required—you need to clone the most recent DPE definition to get the latest updates.
* The recommended practice is to include the release (e.g., Winter 26) in the name of a cloned DPE definition so you know which version it is. 
* When using DPE, there are two runtime platforms that the DPE definition can run on–CRM Analytics and Data Cloud. Most of the NPC definitions are created using CRM Analytics, with only the CSV Import definition using Data Cloud. In general you will want to select CRM Analytics if you are processing data that is in Salesforce objects (i.e., not in Data Cloud DMO objects or Calculated Insights).
* When creating scheduled flows to automatically update your DPE definitions, it is important to consider timing and sequencing. If separate definitions referencing the same object(s) run at the same time, the runs may fail. Avoid this by scheduling runs at least 15 minutes apart. 
* Consider the sequence of your DPE definition scheduled runs. Are there any dependencies that require a certain definition to run before another?
    * Example: your custom DPE definition relies on updated donation totals, so needs to run after the Donor Gift Summary DPE definition completes
* In multicurrency orgs, the currency of the Writeback User is used for calculations
* Household accounts need to have a [Party Relationship Group record](https://sfdo-community-sprints.github.io/npc-best-practices/stakeholder-management/stakeholder-management-prerequisites/#householdswhats-different), and individuals need Account-Contact Relationships with the Household Account for the Donor Gift Summary DPE Definition to summarize correctly.

**Maintaining DPE Definitions from Standard Templates**

Salesforce releases periodic updates to the out-of-the-box DPE definitions it provides. 



* To use an updated definition, you need to clone and activate it in the same way you did at implementation. 
* The DPE definitions, particularly the ones for Fundraising, have had regular updates to them released. 
* Before a new Salesforce release is pushed to production, if the release notes indicate a DPE definition that you’re using has been updated, you may need to review your DPE definitions and test them in a sandbox

After a Salesforce release, you may need to review and test DPE definitions in a sandbox before activating in production. Check the release notes to see if a DPE definition that you’re using has been updated.

Generally, any time you create a new DPE definition, you will need to update the flow action referenced in your schedule triggered flows to make sure they are referencing the most current version of your DPE. 

For the three fundraising DPE's, Salesforce has provided a flow template and flow action that will automatically reference the most current version of those three DPE definitions. You can find more detail about the template [here](https://help.salesforce.com/s/articleView?id=sfdo.fundraising_set_up_automatic_updates_for_fundraising_rollups.htm&type=5). 



* Careful consideration is needed before setting up automatic updates.
* This is a process Salesforce has developed to enable admins to automatically keep clones of the base NPC DPE definitions up to date with each release.
* If you choose this process, definitely do NOT customize the cloned DPE definitions—the automatic updates will overwrite any customizations in the cloned DPE definitions.
* All customizations should be in separate DPE definitions, which will be unaffected by the above process.
    * You can trigger multiple DPE definitions in a single Flow (e.g. your Flow can run the cloned DPE definition first, then run any other DPE definitions after).
* You may not want automatic updates without testing first—it’s important to make sure the newly updated definition is compatible with your Salesforce org and produces expected results.

### **Monitoring & Troubleshooting**

**Monitoring DPE Definitions**

You can monitor DPE Definitions that are run in Setup → Monitor Workflow Services
Results are saved for 30 days
If you have DPE definitions that are using the CRM Analytics platform, the Data Manager app also provides visibility into what happens in the background. It can be used to see Data Sources and other items about the data pipeline job processing. Currently, all the out-of-the-box Nonprofit Cloud DPE definitions use CRM Analytics for processing.
To access the app, go to Setup → Analytics → Data Pipeline → Getting Started, or you can access the app in the Salesforce UI by searching for it in the App Launcher.
See this help article for an overview of the Data Manager App

Here are a few screenshots of “Monitor Workflow Services”:

<img width="700" height="auto" alt="Monitor WFS 1" src="https://github.com/user-attachments/assets/e99ef991-5f34-400c-8bb5-cab82d54866b" />
<br>
<br>
<img width="700" height="auto" alt="Monitor WFS 2" src="https://github.com/user-attachments/assets/4c83d35c-119f-451c-a7d8-5a191f936299" />
<br>
<br>
<img width="700" height="auto" alt="Monitor WFS 3" src="https://github.com/user-attachments/assets/19100501-2779-4b8d-98da-78090691c227" />
<br>
<br>

**Troubleshooting DPE Definitions**



* Verify under Setup → Quick Find  → Data Pipelines that Data Pipelines is enabled and the Data Pipeline for “Salesforce” is checked
* Make sure the Writeback User and Automated Workflow User have the “Data Pipelines Base User” permission set assigned
* Make sure the Integration User has at least Read access to data which is aggregated using the DPE definition
* Under Setup → Quick find  → Monitor Workflow Services find the name of the DPE Definition that was run and check the Status column to see if the Status is “Completed” (ran successfully) or if it “Completed With Failures” or “Failed”.
    * Click the name of the DPE definition for more details about the outcome
* Note that the underlying reporting engine language (SAQL) is case sensitive, so for example, if you have a boolean condition, ‘true’ works but ‘True’ does not
* [Troubleshoot Data Processing Engine Issues](https://help.salesforce.com/s/articleView?id=ind.dpe_troubleshoot.htm&type=5)


### Building a Custom DPE Definition

**What If You Need Calculations That Aren’t Part of the Standard DPE Definition?**

First, determine whether your use case is a good fit for DPE. DPE is recommended for bulk, asynchronous processing and should not be used for real-time calculations. Flow, [Declarative Lookup Rollup Summary (DLRS)](https://sfdo-community-sprints.github.io/DLRS-Documentation/), and other rollup apps are still good go-to tools for real-time rollups and concatenating data.

To avoid having to recreate your custom calculations for each Salesforce release, we recommend you create a new DPE definition versus adding your new calculation(s) to a cloned standard DPE definition. It can also get tricky to add new logic to the more complicated NPC DPE definitions!

The [Data Processing Engine Basics](https://trailhead.salesforce.com/content/learn/modules/data-processing-engine-basics) and [Create Fundraising Rollups in Data Processing Engine](https://trailhead.salesforce.com/content/learn/projects/create-fundraising-rollups-with-data-processing-engine?trailmix_creator_id=strailhead&trailmix_slug=prepare-for-your-salesforce-nonprofit-cloud-consultant-npc-cred) Trailhead badges are a great place to start learning how to build your own DPE definitions. After completing these modules, open up the NPC DPE definitions and look at how they are built. The Donor Gift Summary in particular is the most complex of the standard DPE definitions, but is a good example of how a sophisticated set of calculations can be handled. 

**Considerations When Building a Custom DPE Definition**

* The DPE may run successfully but yield incorrect totals if the calculations aren’t built correctly
* As part of validating your results, consider:
    * Are the filters correct?
    * Are the calculations correct?
    * Are the types of joins correct? 
* Keep in mind that by definition, each data source includes all records of that object, so you will usually need to filter the records
* DPE works best on rollups of quantitative data. If you are looking to concatenate text or picklist values, other tools (e.g. Flow, DLRS) may be a better option.
* If the objects / fields referenced in one of your custom DPE definitions changes, you may need to update your definition.
* To make minor changes to a custom DPE definition, you need to deactivate it, make your updates, save, and then **Activate** again.
    * Keep in mind that DPE doesn’t automatically version definitions the way Flow does. If you want to preserve a previous version, save as a new definition, make the changes, and activate. Don’t forget to deactivate the old version.
    * If you need to back up your current definition, you can download the JSON file using the icon highlighted here. You can create a new definition from your backup by uploading the JSON file.

**Helpful Skill Sets for Customizing and Configuring DPE**

There are several skills that are helpful, maybe even required, when working with DPE. Building these skills prior to creating a custom DPE will support you in creating a DPE that functions correctly. Those skills include: 


* Data Analytics concepts (e.g., inner and outer joins)
* CRM Analytics/Data Cloud 
* Flows
* Salesforce Administrator - Advanced
* Deep understanding of NPC Data Model
