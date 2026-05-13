# Data Schema

This document defines the core Google Sheets tables required for MY-Trade-Journal.

---

## Assets Table

Tracks tradable and watchlist assets.

Required fields:

- ticker
- asset name
- halal status
- liquidity
- asset type
- sector
- reference asset
- correlation score
- volatility level
- approved for execution
- notes

---

## Signals Table

Tracks every market signal, even skipped ones.

Required fields:

- signal ID
- alert timestamp
- market open timestamp
- reference asset
- execution asset
- gap size
- gap direction
- confidence score
- market regime
- trade window status
- setup expiry timestamp
- decision
- reasoning
- logged automatically
- reviewed manually

---

## Trades Table

Tracks actual trades.

Required fields:

- trade ID
- alert timestamp
- market open timestamp
- execution window
- actual entry timestamp
- setup expiry timestamp
- session type
- market phase
- entry price
- exit price
- stop-loss
- position size
- risk amount
- profit/loss
- trade status
- rule followed
- review notes

---

## Behaviour Table

Tracks discipline and execution quality.

Required fields:

- FOMO trade
- revenge trade
- rule violation
- emotional override
- trade taken outside allowed window
- late-session chase entry
- entry during high-spread condition
- entry before confirmation window
- skipped valid trade
- reason for override
- lesson learned

---

## Portfolio Table

Tracks long-term holdings.

Required fields:

- asset
- allocation percentage
- current value
- invested amount
- unrealised profit/loss
- drawdown from recent high
- risk status
- action required
- rebalance required
- review date
