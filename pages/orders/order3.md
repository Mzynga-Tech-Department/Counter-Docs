## Order3

**Route:** `/order3`

**Purpose:** 
Displays locked order details and payment instructions; Order enters pending state.

**Props:**

Takes the order ID from url.

**State**

None ATM.

**Data displayed:**
| Field | Example shown |
|---|---|
| Ethereum price for this transaction | Ksh 245,000 |
| Payment amount | Ksh 18,500 |
| Paybill number | 4107329 |
| Receiving ETH amount | 0.5 Eth |
| Receiving address | pokt132v39vh24y7z8hyhs43fq5pezuasfmt2smq3gl |
| Account number (for paybill payment) | ORDER2354 |
| Order status | PENDING PAYMENT |

**API calls:**
https://api.mzynga.com/readorder?id=${_id}

**Actions**
| Control | Behavior |
|---|---|
| Next | `/order4` |

**Validation:**

* N/A — display-only screen, no inputs.

**Known issues / open questions:**

 - No room to cancel the order at this point

Source https://github.com/MikeMwambia-TrojanSystem/UI-Counter/blob/main/src/pages/order3.jsx
