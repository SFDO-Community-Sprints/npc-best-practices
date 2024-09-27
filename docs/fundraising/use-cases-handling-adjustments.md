---
layout: default
title: Handling Adjustments
nav_order: 8
parent: Fundraising Use Cases
---

# Handling Adjustments
*Last Updated:*

### How to Leverage Gift Refund

Definition:  A gift refund refers to the monetary return of a donation to a donor, typically due to requests, errors, or other valid reasons. This process can be initiated for various reasons such as donor dissatisfaction, a mistake in the donation amount, or return of items related to fundraising efforts. Proper management of gift refunds is essential for maintaining donor trust and satisfaction.

Example: 

Scenario 1:  **Processing a Gift Refund : **

A donor requests a refund. The flow checks eligibility and processes the refund, notifying the donor via email.

Scenario 2 :** Program Cancellation:**

A donor contributes to a specific project that is subsequently cancelled. They request a refund for their donation due to the project not proceeding.

Steps for Implementing Gift Refunds



1. Establish a Gift Refund Policy :
* Define the conditions under which refunds will be processed (e.g, time limits).
* Document the policy for staffing training and donor communication.
2. Configure Salesforce to provide full or Partial Refund:
* From the App Launcher (App Launcher), find and select Gift Transactions.
* Click the paid gift transaction that you want to process a refund for.
* Click Related, and in the Gift Refunds section, click New.
* Enter the refund amount and the refund date.
* Select the refund status
* Save your changes.
* In the gift transaction record, update the status field as needed.
3. Develop a Refund Request Form:
* Create an online form (using Experience Cloud or a similar tool) for donors to submit refund requests.
* Include fields for all required information, ensuring clarity and ease of use.
4. Process the Refund:
* Upon approval, initiate the refund through the organisation's payment processing system (e.g., PayPal, Stripe).
* Update the original donation record in Salesforce to reflect the refund status.
5. Notify the Donors of Refund Status:
* Set up automated email notifications to inform donors about the approval or denial of their refund request.
* Provide details about the refund process and expected timelines
6. Collect Feedback Post-Refund:
* Follow up with donors to gather feedback on their refund experience.
* Use this feedback to improve the refund process and donor relations. 

Prerequisites for Salesforce Admin:

See Prerequisites for Salesforce Admin from [Multiple Payment Gift](use-cases-multiple-payment-gift.md).


Required:



*  Donation Object: Tracks contributions made by donors, including fields such as Donation ID, Amount, Date, and Donor Name.
* Gift Refund Object: Custom object to manage refund requests, with fields such as Refund Amount, Donation ID (lookup), Reason for Refund, and Status (Pending, Approved, Denied).

	

**Prerequisites for End User:**



* See Prerequisites for End User from [Multiple Payment Gift](use-cases-multiple-payment-gift.md).
/
* Required : Ability to navigate the donation records and access the refund request form. Organization’s gift refund policy and timelines for requesting refunds. 

**Best Practices:**



* See Best Practices from [Multiple Payment Gift](use-cases-multiple-payment-gift.md)
.
* Regularly maintain accurate data in the Donation and Gift Refund objects to ensure smooth operations and compliance.
* After processing refunds, solicit feedback from donors about their experience. Use this feedback to improve the process.
