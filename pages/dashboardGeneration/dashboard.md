## dashboard

**Route:** `/dashboard`

**Purpose:** 
Displays infomation about the dashboard and the sell orders that are open to the public

**Props**
Requires a block number and an authentication signature
MainDashboard component

**State**
Requires an active dashboard state

**Data displayed**
| Field | Example shown |
|---|---|
| Counter name | counter_name |
| Dollar rate | Ksh 130 |
| Price in Kshs | 345,678 |
| Avialable Bal | 0.5 Eth |
| Valued at Kshs | 345,658 |
| Max. buy | 150,000 |
| Min. buy | 1,500 |
| Creation Time | 20:00 PM |
| Expiry Time | 02:00 AM |

**API calls**
https://api.mzynga.com/getactivedashboard

**Actions**
| Control | Behavior |
|---|---|
| Buy | `/order` |

**Validation**
RPC Health check every 5 seconds

**Known issues / open questions**
 - Pending Testing

See https://counter-ui-delta.vercel.app/dashboard 
Subject to change

Source https://github.com/MikeMwambia-TrojanSystem/UI-Counter/blob/main/src/pages/dashboard.jsx

RPC is powered by https://api.pocket.network


