---
title: Fundraising Use Cases
parent: Fundraising
nav_order: 1
has_children: true
---
# Fundraising Use Cases

# Overall Considerations

## Gift Commitments
    * When using Gift Entry to update that a Gift Transaction was paid against an existing Gift Commitment with a Gift Commitment Schedule, note that only one payment can be recorded per Gift Transaction. If the payment is lower than the expected Gift Transaction amount, the Gift Transaction will still retain the same name (i.e. the name will reflect the expected amount instead of what was actually paid). Once Gift Entry has processed the Gift Transaction, any edits will require multiple steps and manipulation of the Gift Transaction status.
    * Only one gift entry can be applied per gift commitment transaction. Gift entries of lower amounts can be applied to a commitment transaction of a higher amount. Once a gift commitment is applied to a gift entry, it cannot be removed (Gift Processing Status = Success). Gift Transaction will autoname to the commitment amount, even if the entry amount is different (based on default). Gift Transaction can be edited, but it requires multiple steps and manipulation of the status.
    * In order for the Gift Commitment to appear in Gift Entry it must meet the following criteria:
        * Effective Start Date must be populated
        * Status must be Active
        * Transaction Due Date on scheduled Gift Transaction must match Gift Received Date selected on Gift Entry
    * Gift Commitment must have an effective start date populated for the Gift Commitment to populate on gift entry.
## Gift Batching
    * To remove an entry from a batch, edit from the entry page. Using delete from the batch screen will delete the entry entirely.
    * "Set as Default" checkbox will autofill all fields exactly as set (including donor information) for each gift. Default will remain even if you exit and then return to the batch.
## Deleting 
    * Deleting a gift entry does not automatically delete the related transaction.  The transaction must be deleted separately.
## Other
    * Default automation: Transaction status will be “pending” after entry, except for a cash payment which will have a status of “paid”.
## Gift Designations
    * Be aware of [the inheritance hierarchy for Gift Designations](https://help.salesforce.com/s/articleView?id=sfdo.npc_fr_manage_designations.htm&type=5).

