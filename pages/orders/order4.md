## Order4

**Route:** `/order4`

**Purpose:** 
Buyer submits their M-Pesa payment code to verify payment was made.

**Props:**
None ATM

**State:**
Payment status - default to false.

**Form fields**
| Field | Example | Type | Required? |
|---|---|---|---|
| M-Pesa payment code | UFOHH8E4XY | string | yes |

**API calls**
https://api.mzynga.com/queryreciept?TransID=${pay_code}

**Actions**
| Control | Behavior |
|---|---|
| Verify | `/order5` |

**Validation**

MPESA Code is validated.

**Known issues / open questions**
- Pending testing

Source https://github.com/MikeMwambia-TrojanSystem/UI-Counter/blob/main/src/pages/order4.jsx


