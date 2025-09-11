---
layout: default
title: Data Processing Engine
nav_order: 5
parent: Industry Common Components
---
# Building a Custom DPE Definition

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
