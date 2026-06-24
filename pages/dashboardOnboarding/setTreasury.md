## setTreasury

**Route:** `/setTreasury`

**Purpose:** 
This page captures the information about the treasury,the balance and the withdrawal address of the treasury.

**Props**
None ATM

**State**
None ATM.

**Form fields**
| Field | Example | Type | Required ? |
|---|---|---|---|
| Name | pokt132v39vh24y7z8hyhs43fq5pezuasfmt2smq3gl | String | YES |
| Address balance | 0 | Number | YES |
| Withdrawal address | kangethe.eth | String| | YES


**API calls**
https://api.mzynga.com/createtreasury

**Actions**
| Control | Behavior |
|---|---|
| Save Treasury | `seeDashboard` |

**Validation**
All fields are required

**Known issues / open questions**
- None noted
- Pending testing

See https://counter-ui-delta.vercel.app/setTreasury 
Subject to change

Source https://github.com/MikeMwambia-TrojanSystem/UI-Counter/blob/main/src/pages/setTreasury.jsx