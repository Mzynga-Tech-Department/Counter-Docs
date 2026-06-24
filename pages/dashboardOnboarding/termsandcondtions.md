## Terms and Conditions

**Route:** `/termsandcondtions`

**Purpose:** 
The user at this point is presented with the terms and conditions he has to abide to.
This is done to abide to laws governing the region where counter service is offered.

**Props:**
None

**State:**
* isTaxes
* isPrices
* isSafe
* iswithdrawalA
* isTrade
These are the states that are set by the checkboxes on this page.

**Data displayed**
5 checkboxes:
* Responsibility for filing tax returns
* Responsibility for pricing assets
* Responsibility for paybill safety
* Responsibility for withdrawal address safety/control
* Responsibility for loss/profit from trades

**API calls:**
None atm

**Actions:**
| Control | Behavior |
|---|---|
| Confirm button (currently labeled "YEAH WHEREVER") | `instructions` |

**Validation:**

ALL checkboxes **must** be ticked before you can navigate to next page.

**Known issues / open questions:**
- Button label ("YEAH WHEREVER") reads as placeholder/dev copy — confirm if intentional before shipping.
- Request opinions on the wording for this page.

 **See** https://counter-ui-delta.vercel.app/termsandcondtions 
 Subject to change

 **Source** https://github.com/MikeMwambia-TrojanSystem/UI-Counter/blob/main/src/pages/termsandcondtions.jsx
