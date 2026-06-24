## Order5

**Route:** `/order5`

**Purpose:** 
Final confirmation screen — payment verified, order marked complete, displays transaction summary.

**Props:**
Gets the order ID from url.

**State:**
None ATM

**Data displayed**
| Field | Example shown |
|---|---|
| M-Pesa pay code | 4QA3456G — Payment received |
| ETH receiving address | pokt132v39vh24y7z8hyhs43fq5pezuasfmt2smq3gl |
| Ethereum amount | 0.5 |
| Amount paid (Kshs) | 100,000 |
| Order status | Completed |
| Settlement note | ~15 secs for ETH to be sent and reflect on the receiving address, after which order status updates |

**API calls:**
https://api.mzynga.com/readorder?id=${order_id}

**Actions**
| Control | Behavior |
|---|---|
| Return to Dashboard | `/dashboard` |

**Validation:**

N/A — display-only confirmation screen.

**Known issues / open questions**
- Pending testing
- Pending refactoring
