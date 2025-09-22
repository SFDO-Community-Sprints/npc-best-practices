---
layout: default
title: Setup Steps for Standard DPE Definitions
nav_order: 2
parent: Data Processing Engine
---

# **Setup Steps for Standard DPE Definitions**

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
   - e. **Aggregate Benefit Disbursement and Benefit Assignment**: Updates fields on Benefit and Program Enrollment records. There is also a flex card that can be added to the page layouts.
   - f. **Calculate Benefit Session and Program Enrollment Attendance Rate**: Update fields on the Program Enrollment and Benefit Session. The data included in the attendance summary includes the number of people who attended, the number of people who were marked as absent, and the overall rate of attendance for the session.


For a step-by-step run-through of steps 6 & 7 see [Prepare for Your New Rollups ](https://trailhead.salesforce.com/content/learn/projects/create-fundraising-rollups-with-data-processing-engine/prepare-for-your-new-rollups)on Trailhead.
