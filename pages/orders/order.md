## Order

**Route:** `/order`

**Purpose:** 
Order summary screen shown before a buyer commits to an order.

Displays the dashboard's current rate and purchase limits.

**Props:**
Requires all the information about the order from URL

**State:**
None ATM

**Data displayed:**
| Field | Example shown | Source |
|---|---|---|
| Dashbaord ID |  | |
| Order Status | true/false | |
| Timestamp |  | |
| KES Price |  | |
| Minimum Buy |  | |
| Asset Treasury |  | |

**API calls**
https://api.mzynga.com/createorder

**Actions:**
| Control | Behavior |
|---|---|
| Lock order | `/order1` |
| Return to dashboard | `/dashboard` |

**Validation:**

**ALL** fields are validated before order is created.

**Known issues / open questions:**
- Pending testing.

 **Source** https://github.com/MikeMwambia-TrojanSystem/UI-Counter/blob/main/src/pages/order.jsx
