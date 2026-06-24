## setProfile

**Route:** `/setProfile`

**Purpose:** 
Form to create a new dashboard profile.


**Props**
None atm

**State**
isDisabled
min_buy

**Form fields**
| Field | Example | Type | Required ? |
|---|---|---|---|
| Name | profile_Name | String | YES |
| Paybill number | 4107329 | Number | YES |
| Unique link | kangethe | String| | YES
| Timestamp created | 6/20/2026 | Timestamp | YES |
| Maximum buy amount (Kshs) | 150000 | Number | YES |
| Minimum buy amount (Kshs) | 150 |Number | YES |
| Dollar rate | 130 | Number| YES |

**API calls**
https://api.mzynga.com/createprofile

**Actions**
| Control | Behavior |
|---|---|
| Submit | `setAsset` |

**Validation**
All fields are validated to their type and logic.
Some are editable others are not.

**Known issues / open questions**
None atm

 See https://counter-ui-delta.vercel.app/setProfile 
 Subject to change

 Source https://github.com/MikeMwambia-TrojanSystem/UI-Counter/blob/main/src/pages/setProfile.jsx

