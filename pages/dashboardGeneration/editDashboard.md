## EditDashboard

**Route:** `/editDashboard`

**Purpose:** 
Allows the user to change the information about the dashboard,some information is not editable.

**Props:**
Requires dashboard ID from the url.

**State:**
None ATM

**Data displayed**
| Field | Example shown |
|---|---|
| Dashboard Name | kangethe |
| Dollar Rate | KES 210 |
| Origin Address | mzynga.eth |
| Minimum Amount | KES 100 |

**API calls**
 https://api.mzynga.com/updatedashboard

**Actions**
| Control | Behavior |
|---|---|
| Update Dashboard | `/listDashboard` |

**Validation:**
All inputs are validated.

**Known issues / open questions:**
Pending testing.

See https://counter-ui-delta.vercel.app/editDashboard 
Subject to change

Source https://github.com/MikeMwambia-TrojanSystem/UI-Counter/blob/main/src/pages/editDashboard.jsx
