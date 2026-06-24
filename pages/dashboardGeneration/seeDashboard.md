## seeDashboard

**Route:** `/seeDashboard`

**Purpose:** 
Displays dashboard specific information about:
- Assigned dashboard name - dashboardname
* Configured paybill account - paybill
* Dollar(assuming it's priced in $) to KES exchange rate - dollar_rate
* Asset selected to be sold on the dashboard - asset_id
* Dashbaord treasury wallet - asset_treasury
* Withdrawal address of the dashboard - origin_Address
* Maximum purchase in KES - maximum_buy_kshs
* Minimum purchase in KES - minimum_buy_kshs

**Props:**
* None ATM

**State:**
* treasurySt
* profileSt
* priceInfoSt
* priceInfoStKshs
* dashboardSt

**Data displayed**
| Field | Example shown |
|---|---|
| Dashboard name | KangetheDashbaord |
| Paybill | 4107329 |
| Dollar rate | 130 |
| Asset treasury | mzynga.eth |
| Origin Address | pokt132v39vh24y7z8hyhs43fq5pezuasfmt2smq3gl |
| Maximum buy  | 150,000 |
| Minimum buy | 150 |

**API calls**
https://api.mzynga.com/createdashboard

**Actions**
| Control | Behavior |
|---|---|
| Next | `listDashboard` |

**Validation:**
N/A — display-only screen, no inputs.

**Known issues / open questions:**
Pending testing

See https://counter-ui-delta.vercel.app/seeDashboard 
Subject to change

Source https://github.com/MikeMwambia-TrojanSystem/UI-Counter/blob/main/src/pages/seeDashboard.jsx

