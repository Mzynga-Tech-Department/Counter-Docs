## Order1

**Route:** `/order1`

**Purpose:** 
Buyer enters the KES amount they want to spend.

**Props:**
Requires **ALL** the information about the order from URL.

**State:**
None atm

**Form fields:**
| Field | Example | Type | Required |
|---|---|---|---|
| KES amount to spend | (free input) | numeric | yes |

**Data displayed:**
- Maximum buy per transaction (Kshs) — pulled from dashboard configuration.
- Minimum buy per transaction (Kshs) — pulled from dashboard configuration.

**API calls:**
https://api.mzynga.com/updateorder

**Actions:**
| Control | Behavior |
|---|---|
| Next | `/order2` |

**Validation:**

Next is disabled until the amount is validated.

**Known issues / open questions:**

- No way to cancel order at this point.
- Pending testing.

 Source https://github.com/MikeMwambia-TrojanSystem/UI-Counter/blob/main/src/pages/order1.jsx

