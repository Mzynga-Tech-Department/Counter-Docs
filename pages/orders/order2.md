## Order2

**Route:** `/order2`

**Purpose:** 
Buyer enters the destination crypto address for the Ethereum tokens.

**Props**
Requires **ALL** the information about the order from URL.

**State:**
None atm

**Form fields:**
| Field | Example | Type | Required |
|---|---|---|---|
| Receiving crypto address | (free input) | string, address format | yes |

**API calls:**
https://api.mzynga.com/updateorder

**Actions:**
| Control | Behavior |
|---|---|
| Validate order | `/order3` |

**Validation:**
The address is verified whether it is an ethereum address and not a smart contract address.It must be an externally owned account (EOA).
The address **MUST** verify for the button to activate.

**Known issues / open questions:**
- Pending testing

Source https://github.com/MikeMwambia-TrojanSystem/UI-Counter/blob/main/src/pages/order2.jsx
