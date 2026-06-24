## instructions

**Route:** `/instructions`

**Purpose:** 
Explains dashboard rules/limits before the user creates one.

**Props**
None ATM

**State**
None ATM

**Data displayed**
- Up to 20 active dashboards per paybill
- Dashboard requires: dollar rate, paybill number, supported asset(s)
- Dollar rate explanation (higher = pricier for buyer, lower = cheaper)
- One paybill per dashboard
- At least one supported asset required to activate; currently only Ethereum Token on Ethereum Mainnet

**API calls**
None

**Actions**
| Control | Behavior |
|---|---|
| Set up dashboards | `setProfile` |

**Validation**
N/A — informational screen, no inputs.

**Known issues / open questions**
None ATM.

See https://counter-ui-delta.vercel.app/instructions 
Subject to change

Source https://github.com/MikeMwambia-TrojanSystem/UI-Counter/blob/main/src/pages/instructions.jsx

