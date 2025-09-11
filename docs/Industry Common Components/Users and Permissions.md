---
layout: default
title: Users & Permissions
nav_order: 1
parent: Data Processing Engine
---
# Users & Permissions

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

## **Relevant Users for Basic Setup**



* **System Administrator**: needs the Data Pipeline Base User permission set assigned
* **Integration User** (assigned the Analytics Cloud Integration User profile): needs at least Read access to every object and field referenced in DPE definitions. Assign the object/field permissions directly to the Analytics Cloud Integration User profile  - you do **NOT** need to assign a Fundraising Access permission set license to the Integration User.
* **Writeback User:** needs full CRED access to all objects and fields referenced in the definition
    * This is the user that the DPE uses to create and update records, and is specified in the Writeback nodes of the definition
    * Must have permissions to create/read/edit/delete
    * Note that the Writeback User defaults to the Default Workflow User ([set in Process Automation Settings](https://help.salesforce.com/s/articleView?id=platform.workflow_defaultuser.htm&type=5)), but does not have to be the same user.
