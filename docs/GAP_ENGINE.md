# Gap Opportunity Engine

The Gap Opportunity Engine is designed for short-term tactical opportunities based on market open gap behaviour.

It is not designed for emotional trading or forced daily trades.

---

## Purpose

This engine is designed for:

- short-term tactical opportunities
- market open gap analysis
- continuation setup tracking
- statistical edge building
- behaviour control

---

## Actions

- BUY
- WAIT
- SKIP
- EXIT
- LOCK

---

## Core Logic

```text
IF asset is not halal-approved
    → SKIP

IF gap is weak
    → SKIP

IF volatility is extreme
    → WAIT

IF trade window is not active
    → WAIT or SKIP

IF setup confirmation has expired
    → SKIP

IF daily loss limit is reached
    → LOCK

IF setup score is high
AND risk rules pass
AND confirmation is valid
    → BUY
```

---

## Trade Window Rules

The engine must include time-based execution rules.

Trade windows are used to:

- avoid emotional entries at market open
- avoid chasing late moves
- measure which session windows perform best
- identify behavioural failure patterns by time of day
- stop the system from acting when the opportunity has expired

---

## Core Trade Window

For US market reference assets:

| Rule | Time |
|---|---|
| Market open | 09:30 ET |
| Avoid first open volatility | first 1–3 minutes |
| Earliest allowed entry | 09:35 ET |
| Preferred confirmation window | 09:45–10:30 ET |
| Decay window | 10:30–11:00 ET |
| Setup validity expiry | 11:00 ET |
| After expiry | skip by default |

No chasing after expiry unless a separate high-quality continuation rule is triggered.

---

## Time-Based Decision Rules

```text
IF current time is before allowed entry window
    → WAIT

IF price has not confirmed by setup expiry time
    → SKIP

IF spread is abnormal during open volatility
    → WAIT

IF trade is taken outside preferred window
    → FLAG FOR REVIEW

IF late-session entry is attempted without stronger confirmation
    → BLOCK
```

---

## Session Types

| Session Phase | Meaning | Default Action |
|---|---|---|
| Pre-market | Before official market open | WATCH ONLY |
| Opening volatility | First 1–5 minutes | WAIT |
| Confirmation window | 09:45–10:30 ET | TRADE ALLOWED IF RULES PASS |
| Decay window | 10:30–11:00 ET | TRADE ONLY IF STRONG |
| Expired window | After 11:00 ET | SKIP BY DEFAULT |
| Late session | Afternoon / near close | STRONG CONFIRMATION REQUIRED |

---

## Required Trade Window Fields

Every gap alert and trade log must include:

- alert timestamp
- market open timestamp
- execution window
- earliest allowed entry time
- preferred confirmation window
- setup expiry timestamp
- actual entry timestamp
- session type
- market phase
- trade window status
- whether the entry was inside or outside the allowed window
