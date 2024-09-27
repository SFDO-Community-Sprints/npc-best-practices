---
layout: default
title: Gift from Donor-Advised Fund
nav_order: 7
parent: Fundraising Use Cases
---

# Gift from Donor-Advised Fund
*Last Updated:*

Represented by Gift Transactions, Gift Commitment, Gift Commitment Schedule, Gift Soft Credits (Opportunity optional)

Consider Partner resource listed in [References](https://docs.google.com/document/d/1R4sRRd1VSMeSmUbVenMY6ci_GE0FLp_FR0fYu99xvYs/edit#heading=h.j1lq2yn0gzbk)

**Definition:**



* Gift is from a charitable account where a party (a donor) is eligible to take an immediate tax deduction when cash or securities are donated
    * The funds are invested for tax-free growth and the assets can be donated to a charitable organization. 
* Gift can be an outright gift (paid at time of record creation) or a pledged gift (promised to be paid at a later date)
* Gift is hard-credited to the donor-advised fund (DAF), and soft-credited to the donors within the DAF

**Examples:**



* Alex Brown makes an outright gift to Fidelity Charitable Gift Fund. Fidelity includes that transaction in their next payment to the charity. Fidelity receives the hard credit and Alex Brown receives the soft credit for the gift. 
* Alex Brown sets up a recurring payment to Fidelity Charitable Gift Fund. Fidelity includes the pledged gift in its ongoing payments to the charity. When the pledge is created, Alex Brown gets the hard credit for the gift. When the gift has been received, the gift is updated to give Fidelity the hard credit and Alex Brown the soft credit. 

**Optional (creating/linking to an) Opportunity because:**



* Tracking solicitation may not be necessary

**Prerequisites for Salesforce Admin:**



* See [Prerequisites for Salesforce Admin](https://docs.google.com/document/d/1R4sRRd1VSMeSmUbVenMY6ci_GE0FLp_FR0fYu99xvYs/edit#bookmark=id.ds0z7f6syy7y) from Use Case #2
* Required	
    * Confirm that Gift Soft Credits are available on the Gift Entry template and Gift Transaction related list
* Optional
    * Add Pledge record type to Gift Commitment (as advised in Salesforce documentation)

**Prerequisites for End User:**



* See [Prerequisites for End User](https://docs.google.com/document/d/1R4sRRd1VSMeSmUbVenMY6ci_GE0FLp_FR0fYu99xvYs/edit#bookmark=id.5m49q85t9gqk) from Use Case #2
* Required
    * Ensure that a Business Account exists for the donor-advised fund provider (e.g. Fidelity Charitable Gift Fund)
    * Ensure that a Person Account exists for each specified donor
* Optional
    * Ensure that a Business Account exists for the specific donor’s donor-advised fund (e.g. Fidelity Charitable Gift Fund - Alex Brown Fund). Link this Account to the donor-advised fund provider Account using Account hierarchy. The donor-advised fund provider should be the Parent Account.

**Best Practices:**



* See [Best Practices](https://docs.google.com/document/d/1R4sRRd1VSMeSmUbVenMY6ci_GE0FLp_FR0fYu99xvYs/edit#bookmark=id.yiq4ie45xakc) from Use Case #2
* Use a specific donor’s donor-advised fund to make donation tracking easier. 
* Create the Gift Commitment Schedule right after creating the Gift Commitment. This will automatically create the related Gift Transactions. 

**How to enter the gift via Gift Entry:**



* See [How to enter the gift via Gift Entry](https://docs.google.com/document/d/1R4sRRd1VSMeSmUbVenMY6ci_GE0FLp_FR0fYu99xvYs/edit#bookmark=id.4h03b9rj3yn) from Use Case #2
* Set Gift Type to Organization/Household
* Set Donor as the donor-advised fund provider or the specific donor’s donor-advised fund Account
* Set Soft Credit information (will only appear when Gift Amount is added) to ensure the specific donor receives a soft credit. Set Role to Third-party donor.

**How to enter the gift without Gift Entry (recommended):**



* See [How to enter the gift (without Gift Entry)](https://docs.google.com/document/d/1R4sRRd1VSMeSmUbVenMY6ci_GE0FLp_FR0fYu99xvYs/edit#bookmark=id.jvrs20w0kfak) from Use Case #2
* Ensure that the Gift Transaction is created/updated to:
    * Set Gift Type to Organization/Household
    * Set Donor as the donor-advised fund provider or the specific donor’s donor-advised fund Account
* Create a Gift Soft Credit linked to the Gift Transaction to ensure the specific donor receives a soft credit. Set Role to Third-party donor.
