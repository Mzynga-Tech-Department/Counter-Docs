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