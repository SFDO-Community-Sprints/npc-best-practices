---
layout: default
title: Monitoring and Troubleshooting
nav_order: 4
parent: Data Processing Engine
---
# **Monitoring & Troubleshooting**

## **Monitoring DPE Definitions**

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

 ## **Troubleshooting DPE Definitions**



* Verify under Setup → Quick Find  → Data Pipelines that Data Pipelines is enabled and the Data Pipeline for “Salesforce” is checked.
* Make sure the Writeback User and Automated Workflow User have the “Data Pipelines Base User” permission set assigned.
* Make sure the Integration User has at least Read access to data which is aggregated using the DPE definition.
* Under Setup → Quick find  → Monitor Workflow Services find the name of the DPE Definition that was run and check the Status column to see if the Status is “Completed” (ran successfully) or if it “Completed With Failures” or “Failed”.
    * Click the name of the DPE definition for more details about the outcome.
* Note that the underlying reporting engine language (SAQL) is case sensitive. For example, if you have a boolean condition, ‘true’ works but ‘True’ does not.
* [Troubleshoot Data Processing Engine Issues](https://help.salesforce.com/s/articleView?id=ind.dpe_troubleshoot.htm&type=5)
