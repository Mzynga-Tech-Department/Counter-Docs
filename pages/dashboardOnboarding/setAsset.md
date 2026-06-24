## setAsset

**Route:** `/setAsset`

**Purpose:** 
Configures which asset a dashboard sells and it's price source.

**Props:**
None atm

**State:**
* isDisabled
* isUpdate
* price

**Form fields:**
| Field | Example | Type  | Required? |
|---|---|---|---|
| Supported asset | Ethereum (ETH) | read only | fixed |
| Supported chain | Ethereum Sepolia Testnet | read only | fixed |
| Price oracle | Binance (radio select) | read only | only option currently but more planned |
| Dollar price | live, oracle-fed | read-only | YES |
| Minimum sell amount | KES 150 | KES Equivalent | Above KES 150 |

**API calls**
https://api.mzynga.com/createasset

**Actions**
| Control | Behavior |
|---|---|
| Update price | Pulls the price of ETH from the selected Oracle |
| Save | `genMne` |

**Validation:**

All fields are required.

**Known issues / open questions:**
- Save button appears greyed/disabled in current build — confirm intended trigger condition.

See https://counter-ui-delta.vercel.app/setAsset 
Subject to change

Source https://github.com/MikeMwambia-TrojanSystem/UI-Counter/blob/main/src/pages/setAsset.jsx
