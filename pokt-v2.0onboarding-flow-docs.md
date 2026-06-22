# Onboarding flow — component documentation

Template for documenting each `.jsx` file in the onboarding flow. One section
per file. Fields marked `<!-- fill in -->` need source review to complete —
everything else is pre-filled from the rendered UI.

How to fill out a section:
1. Open the file in the repo
2. Replace each `<!-- fill in -->` with the real value
3. Delete the comment markers once filled
4. Leave `N/A` if a field genuinely doesn't apply (don't delete the row)

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

## Suggested flow order

```
welcome → termsandcondtions → instructions → setProfile → setAsset → genMne → setTreasury
```

<!-- fill in: confirm actual routing logic — can any step be skipped or revisited? is order enforced or just convention? -->
