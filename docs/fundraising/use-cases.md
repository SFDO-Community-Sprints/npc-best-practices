---
title: Fundraising Use Cases
parent: Fundraising
nav_order: 1
has_children: true
---
# Fundraising Use Cases
For nonprofits, incoming monies arrive in various ways and can be recorded in a variety of ways. The Fundraising Use Cases on these pages are meant as a guide to help nonprofits understand how to record and track incoming monies in Salesforce's Nonprofit Cloud.

# Overall Considerations

## Gift Commitments
* When using Gift Entry to update that a Gift Transaction was paid against an existing Gift Commitment with a Gift Commitment Schedule, note that only one payment can be recorded per Gift Transaction.
* Gift Transaction will autoname to the commitment amount, even if the entry amount is different (based on default)
* Once Gift Entry has processed the Gift Transaction, any edits will require multiple steps and manipulation of the Gift Transaction status.
* Once a gift commitment is applied to a gift entry, it cannot be removed (Gift Processing Status = Success).
* Gift Transaction with a status of Paid can be edited, but it requires multiple steps and manipulation of the status. See the documentation [here](https://help.salesforce.com/s/articleView?id=sfdo.npc_fr_gift_transactions.htm&type=5).
* In order for the Gift Commitment to appear in Gift Entry it must meet the following criteria:
    * Effective Start Date must be populated
    * Status must be Active
    * Transaction Due Date on scheduled Gift Transaction must match Gift Received Date selected on Gift Entry
## Gift Entry
* Starting in the Spring '25 release, you can [map custom fields for Gift Entry](https://help.salesforce.com/s/articleView?id=release-notes.rn_fundraising_improve_donor_relations_and_track_the_impact_of_gifts.htm&release=254&type=5).
* At this time, you cannot create Gift Entry templates. The ability to add and use templates was announced at Dreamforce '24 and is on the roadmap for the second half of 2025.
## Gift Batching
* To remove an entry from a batch, edit from the entry page. Using delete from the batch screen will delete the entry entirely.
* "Set as Default" checkbox will autofill all fields exactly as set (including donor information) for each gift. Default will remain even if you exit and then return to the batch.
## Gift Designations
* Be aware of [the inheritance hierarchy for Gift Designations](https://help.salesforce.com/s/articleView?id=sfdo.npc_fr_manage_designations.htm&type=5).
## Deleting 
* Deleting a gift entry does not automatically delete the related transaction.  The transaction must be deleted separately.
## Other
* Default automation: Transaction status will be “pending” after entry, except for a cash payment which will have a status of “paid”.

