# Counter UI — component documentation

Fillable documentation template covering every `.jsx` page in two flows:

1. **Onboarding flow** — desk setup, terms, dashboard/profile/asset/treasury config
2. **Order flow** — buyer-facing purchase of crypto via paybill/M-Pesa

Fields marked `<!-- fill in -->` need source review to complete — everything
else is pre-filled from rendered UI screenshots.

**How to fill out a section**
1. Open the file in the repo
2. Replace each `<!-- fill in -->` with the real value
3. Delete the comment markers once filled
4. Leave `N/A` if a field genuinely doesn't apply (don't delete the row)

---

## Table of contents

**Onboarding flow**
- [welcome.jsx](#welcomejsx)
- [termsandcondtions.jsx](#termsandcondtionsjsx)
- [instructions.jsx](#instructionsjsx)
- [setProfile.jsx](#setprofilejsx)
- [setAsset.jsx](#setassetjsx)
- [genMne.jsx](#genmnejsx)
- [setTreasury.jsx](#settreasuryjsx)
- [Suggested onboarding flow order](#suggested-onboarding-flow-order)

**Order flow**
- [order.jsx](#orderjsx)
- [order1.jsx](#order1jsx)
- [order2.jsx](#order2jsx)
- [order3.jsx](#order3jsx)
- [order4.jsx](#order4jsx)
- [order5.jsx](#order5jsx)
- [Suggested order flow order](#suggested-order-flow-order)

---
---

# Onboarding flow

Covers desk setup: welcome screen, terms acceptance, dashboard instructions,
profile/asset/treasury configuration.

---

## welcome.jsx

**Route:** `/welcome`
**Purpose:** Landing screen confirming desk identity and config before setup begins.

**Props**
<!-- fill in: does this component accept props, or pull everything from route/context? -->

**State**
<!-- fill in: local state variables and what they hold -->

**Data displayed**
| Field | Example shown | Source `<!-- fill in: hardcoded / query param / fetched -->` |
|---|---|---|
| Desk name | Kang'ethe OTC desk Test 1 | |
| Confirmed URL | https://kangethe.counter.co.ke | |
| Supported assets | Ethereum Token on Ethereum Network | |
| Daily KES volume cap | 150,000 | |

**API calls**
<!-- fill in: endpoint(s) called on mount or on submit, request/response shape -->

**Actions**
| Control | Behavior |
|---|---|
| Continue | <!-- fill in: navigates to which route, any side effects? --> |

**Validation**
<!-- fill in: any conditions that block Continue -->

**Known issues / open questions**
<!-- fill in -->

---

## termsandcondtions.jsx

**Route:** `/termsandcondtions`
**Purpose:** Terms acceptance gate before paybill/wallet linking proceeds.

**Props**
<!-- fill in -->

**State**
<!-- fill in: likely one boolean per checkbox — confirm names -->

**Data displayed**
5 checkboxes:
1. Responsibility for filing tax returns
2. Responsibility for pricing assets
3. Responsibility for paybill safety
4. Responsibility for withdrawal address safety/control
5. Responsibility for loss/profit from trades

**API calls**
<!-- fill in: is acceptance logged/timestamped anywhere server-side? -->

**Actions**
| Control | Behavior |
|---|---|
| Confirm button (currently labeled "YEAH WHEREVER") | <!-- fill in: navigates where, writes what --> |

**Validation**
<!-- fill in: are all 5 checkboxes required before the button enables? confirm against source, screenshot is ambiguous -->

**Known issues / open questions**
- Button label ("YEAH WHEREVER") reads as placeholder/dev copy — confirm if intentional before shipping.
<!-- fill in: anything else -->

---

## instructions.jsx

**Route:** `/instructions`
**Purpose:** Explains dashboard rules/limits before the user creates one.

**Props**
<!-- fill in -->

**State**
<!-- fill in -->

**Data displayed**
- Up to 20 active dashboards per paybill
- Dashboard requires: dollar rate, paybill number, supported asset(s)
- Dollar rate explanation (higher = pricier for buyer, lower = cheaper)
- One paybill per dashboard
- At least one supported asset required to activate; currently only Ethereum Token on Ethereum Mainnet

**API calls**
<!-- fill in: is any of this copy dynamic/config-driven, or static text? -->

**Actions**
| Control | Behavior |
|---|---|
| Set up dashboards | <!-- fill in: navigates to setProfile? --> |

**Validation**
N/A — informational screen, no inputs.

**Known issues / open questions**
<!-- fill in -->

---

## setProfile.jsx

**Route:** `/setProfile`
**Purpose:** Form to create a new dashboard profile.

**Props**
<!-- fill in -->

**State**
<!-- fill in: one var per field below, confirm names/types -->

**Form fields**
| Field | Example | Type `<!-- fill in -->` | Required? `<!-- fill in -->` |
|---|---|---|---|
| Name | invoice #1-100000 | | |
| Paybill number | 4107329 | | |
| Unique link | kangethe | | |
| Timestamp created | 6/20/2026 | | auto-set, not user input — confirm |
| Maximum buy amount (Kshs) | 150000 | | |
| Minimum buy amount (Kshs) | 15000 (default shown: 150) | | |
| Dollar rate | 1.02 | | |

**API calls**
<!-- fill in: POST endpoint on submit, payload shape, response handling -->

**Actions**
| Control | Behavior |
|---|---|
| Submit | <!-- fill in --> |

**Validation**
<!-- fill in: min < max enforcement? unique link availability check? required field checks? -->

**Known issues / open questions**
<!-- fill in -->

---

## setAsset.jsx

**Route:** `/setAsset`
**Purpose:** Configures which asset a dashboard sells and its price source.

**Props**
<!-- fill in -->

**State**
<!-- fill in -->

**Form fields**
| Field | Example | Type `<!-- fill in -->` | Required? `<!-- fill in -->` |
|---|---|---|---|
| Supported asset | Ethereum (ETH) | | fixed/selectable? |
| Supported chain | Ethereum Sepolia Testnet | | fixed/selectable? |
| Price oracle | Binance (radio select) | | only option currently — confirm if more planned |
| Dollar price | live, oracle-fed | read-only | |
| Minimum sell amount | $1 | | |

**API calls**
<!-- fill in: oracle endpoint, polling mechanism for the 5-second price refresh -->

**Actions**
| Control | Behavior |
|---|---|
| Update price | <!-- fill in: manual refresh trigger, or confirms a pending value? --> |
| Save | <!-- fill in: appears disabled in current UI — confirm enabling condition --> |

**Validation**
<!-- fill in -->

**Known issues / open questions**
- Save button appears greyed/disabled in current build — confirm intended trigger condition.
<!-- fill in: anything else -->

---

## genMne.jsx

**Route:** `/genMne`
**Purpose:** Generates the mnemonic phrase for the desk's treasury wallet.

**Props**
<!-- fill in -->

**State**
<!-- fill in -->

**Data displayed**
- Warning copy: phrase is the foundation of the wallet; whoever holds it controls the treasury
- Explicit note: phrase is **not stored** by the platform, cannot be recovered if lost

**API calls / library used**
<!-- fill in: which library generates the mnemonic (e.g. ethers, bip39), client-side only or does any data leave the browser? -->

**Actions**
| Control | Behavior |
|---|---|
| Generate mnemonic phrase | <!-- fill in: where is the phrase displayed after click? this screen doesn't show that state --> |

**Validation**
<!-- fill in: is there a confirmation step (e.g. re-enter phrase) before proceeding to setTreasury? -->

**Security notes**
<!-- fill in: confirm phrase never touches a server/log, confirm clipboard handling if copy-to-clipboard exists -->

**Known issues / open questions**
<!-- fill in -->

---

## setTreasury.jsx

**Route:** `/setTreasury`
**Purpose:** <!-- fill in: no screenshot available — likely links the generated wallet/treasury address to the dashboard, confirm from source -->

**Props**
<!-- fill in -->

**State**
<!-- fill in -->

**Data displayed / form fields**
<!-- fill in: needs screenshot or source review -->

**API calls**
<!-- fill in -->

**Actions**
<!-- fill in -->

**Validation**
<!-- fill in -->

**Known issues / open questions**
- No screenshot was available when this doc was drafted — full section needs source review.

---

## Suggested onboarding flow order

```
welcome → termsandcondtions → instructions → setProfile → setAsset → genMne → setTreasury
```

<!-- fill in: confirm actual routing logic — can any step be skipped or revisited? is order enforced or just convention? -->

---
---

# Order flow

Covers the buyer-facing purchase flow: order summary, amount entry, address
entry, payment instructions, M-Pesa code verification, completion.

> **Naming check:** the rendered screens show a buyer paying KES via
> paybill/M-Pesa to receive Ethereum at a POKT-style receiving address. This
> reads as a buy-side transaction from the end user's perspective. Confirm
> "sell" in the codebase/feature name refers to the dashboard owner selling
> crypto to the buyer (i.e. named from the desk operator's point of view)
> before publishing this doc, so the terminology lines up with the rest of
> the repo.

---

## order.jsx

**Route:** `/order`
**Purpose:** Order summary screen shown before a buyer commits to an order — displays the dashboard's current rate and purchase limits.

**Props**
<!-- fill in: dashboard ID likely passed via route param or context — confirm -->

**State**
<!-- fill in -->

**Data displayed**
| Field | Example shown | Source `<!-- fill in: fetched from dashboard config / live oracle -->` |
|---|---|---|
| Dollar rate | Kshs per $1 (value blank in screenshot — confirm rendering bug or just empty test data) | |
| Minimum purchase | KSHs | |
| Maximum purchase | KSHs | |
| Asset price | KSHs for 1.0000 Ethereum at $X | |

**API calls**
<!-- fill in: endpoint fetching dashboard rate/limits, and whether asset price is live-polled here or fetched once on load -->

**Actions**
| Control | Behavior |
|---|---|
| Lock order | <!-- fill in: navigates to order1? does it reserve the rate for a time window? --> |
| Return to dashboard | <!-- fill in: navigates back to which dashboard route --> |

**Validation**
N/A — display-only screen, no inputs.

**Known issues / open questions**
- Screenshot shows blank values for dollar rate, min/max purchase, and dollar price — confirm whether this is a data-loading bug or just an unconfigured test dashboard.

---

## order1.jsx

**Route:** `/order1`
**Purpose:** Buyer enters the KES amount they want to spend.

**Props**
<!-- fill in -->

**State**
<!-- fill in: amount input value -->

**Form fields**
| Field | Example | Type `<!-- fill in -->` | Required? `<!-- fill in -->` |
|---|---|---|---|
| KES amount to spend | (free input) | numeric | yes |

**Data displayed**
- Maximum buy per transaction (Kshs) — pulled from dashboard config
- Minimum buy per transaction (Kshs) — pulled from dashboard config

**API calls**
<!-- fill in: is min/max fetched here or passed down from order.jsx state? -->

**Actions**
| Control | Behavior |
|---|---|
| Next | <!-- fill in: navigates to order2, passes amount forward how (state/context/query param)? --> |

**Validation**
<!-- fill in: confirm Next is disabled until amount is entered and within min/max bounds — button appears greyed/disabled in screenshot -->

**Known issues / open questions**
- Next button appears disabled in the screenshot — confirm exact enabling condition.

---

## order2.jsx

**Route:** `/order2`
**Purpose:** Buyer enters the destination crypto address for the Ethereum.

**Props**
<!-- fill in -->

**State**
<!-- fill in: address input value -->

**Form fields**
| Field | Example | Type `<!-- fill in -->` | Required? `<!-- fill in -->` |
|---|---|---|---|
| Receiving crypto address | (free input) | string, address format | yes |

**API calls**
<!-- fill in: is the address format validated client-side (checksum/regex) or server-side on submit? -->

**Actions**
| Control | Behavior |
|---|---|
| Validate order | <!-- fill in: navigates to order3, what validation runs before proceeding --> |

**Validation**
<!-- fill in: confirm address format check exists — button appears disabled in screenshot, presumably until a valid-looking address is entered -->

**Known issues / open questions**
- Validate order button appears disabled in the screenshot — confirm exact enabling condition (non-empty field vs. actual address format check).

---

## order3.jsx

**Route:** `/order3`
**Purpose:** Displays locked order details and payment instructions; order enters pending state.

**Props**
<!-- fill in -->

**State**
<!-- fill in: order ID, payment status -->

**Data displayed**
| Field | Example shown |
|---|---|
| Ethereum price for this transaction | Ksh 245,000 |
| Payment amount | Ksh 18,500 |
| Paybill number | 4107329 |
| Receiving ETH amount | 0.5 Eth |
| Receiving address | pokt132v39vh24y7z8hyhs43fq5pezuasfmt2smq3gl |
| Account number (for paybill payment) | ORDER2354 |
| Order status | PENDING PAYMENT |

**API calls**
<!-- fill in: is order locked/created via an API call on this page load, or was it created in order2? does this page poll for payment confirmation? -->

**Actions**
| Control | Behavior |
|---|---|
| Next (implied — "click next to enter mpesa payment code") | <!-- fill in: navigates to order4 --> |

**Validation**
N/A — display-only screen, no inputs.

**Known issues / open questions**
<!-- fill in: confirm how long an order stays "locked" before expiring if payment isn't made -->

---

## order4.jsx

**Route:** `/order4`
**Purpose:** Buyer submits their M-Pesa payment code to verify payment was made.

**Props**
<!-- fill in -->

**State**
<!-- fill in: payment code input value -->

**Form fields**
| Field | Example | Type `<!-- fill in -->` | Required? `<!-- fill in -->` |
|---|---|---|---|
| M-Pesa payment code | (free input) | string | yes |

**API calls**
<!-- fill in: endpoint that verifies the M-Pesa code against the paybill transaction — likely calls Safaricom Daraja API or an internal reconciliation service, confirm -->

**Actions**
| Control | Behavior |
|---|---|
| Verify | <!-- fill in: navigates to order5 on success — what happens on failure/invalid code? --> |

**Validation**
<!-- fill in: confirm Verify is disabled until a code is entered — appears disabled in screenshot -->

**Known issues / open questions**
- Verify button appears disabled in the screenshot — confirm exact enabling condition.
- <!-- fill in: confirm error handling/messaging if the entered code doesn't match a real payment -->

---

## order5.jsx

**Route:** `/order5`
**Purpose:** Final confirmation screen — payment verified, order marked complete, displays transaction summary.

**Props**
<!-- fill in -->

**State**
<!-- fill in -->

**Data displayed**
| Field | Example shown |
|---|---|
| M-Pesa pay code | 4QA3456G — Payment received |
| POKT receiving address | pokt132v39vh24y7z8hyhs43fq5pezuasfmt2smq3gl |
| Ethereum amount | 0.5 |
| Amount paid (Kshs) | 100,000 |
| Order status | Completed |
| Settlement note | ~15 secs for ETH to be sent and reflect on the receiving address, after which order status updates |

**API calls**
<!-- fill in: does this page poll the chain/POKT gateway to confirm the ETH transfer landed, or does it just display a static "completed" state once order4's verify call succeeds? -->

**Actions**
<!-- fill in: any actions on this screen (e.g. "return to dashboard", "view on explorer")? not visible in screenshot -->

**Validation**
N/A — display-only confirmation screen.

**Known issues / open questions**
- Amount paid (100,000 Kshs) doesn't match the 18,500 Kshs payment instruction shown in order3 for the same 0.5 ETH — confirm whether this is a data/test inconsistency or whether order3 and order5 represent different transactions reused for screenshots.

---

## Suggested order flow order

```
order → order1 → order2 → order3 → order4 → order5
```

| Step | What happens |
|---|---|
| order | Show dashboard rate/limits, lock the order |
| order1 | Buyer enters KES amount to spend |
| order2 | Buyer enters receiving crypto address |
| order3 | Order locked, payment instructions shown, status = pending |
| order4 | Buyer submits M-Pesa code to verify payment |
| order5 | Payment confirmed, order completed, ETH sent |

<!-- fill in: confirm actual routing logic — can a user go back and edit amount/address after locking in order3? what happens if they abandon mid-flow (does the order expire)? -->
