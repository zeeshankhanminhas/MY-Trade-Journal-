# MY-Trade-Journal

A clean trading operating system for halal-conscious investing, gap opportunities, risk control, and trade journaling.

This project is designed to help build discipline, protect capital, track trading behaviour, and slowly develop a data-backed edge.

---

## Halal Trading Engine — Core Master Project

MY-Trade-Journal is a controlled personal trading and investing system built around two parallel engines:

1. **Long-Term Halal ETF Compound Engine**
2. **Gap Opportunity Engine**

The system is designed around:

- capital protection
- statistical decision making
- halal constraints
- disciplined execution
- behaviour tracking
- long-term sustainability

The aim is not to predict every market move.

The aim is to build a system that knows when to:

- wait
- skip
- reduce risk
- protect capital
- only act when conditions are strong enough

---

## Current Status

This project is currently in the planning and early build stage.

Initial focus:

- manual Google Sheet tracker
- halal asset watchlist
- trade journal
- trade window rules
- gap setup logging
- risk control rules
- alert message structure

Automation will be added gradually using:

- TradingView
- Google Apps Script
- Google Sheets
- Telegram
- Power BI later

---

## Disclaimer

This project is for personal tracking, journaling, research, and system discipline only.

It is not financial advice, investment advice, halal financial advice, or a recommendation to buy or sell any asset.

All trading and investing decisions remain the responsibility of the user.

---

## Core Principles

### 1. Protect Capital First

The system should prioritise survival before growth.

A skipped trade is better than a bad trade.

### 2. Trade With Evidence

Every signal, entry, exit, mistake, and emotional override should be logged.

The system should improve through recorded behaviour and real trade data.

### 3. Follow Halal Constraints

The system avoids:

- futures
- CFDs
- margin trading
- interest-based leverage
- conventional short selling
- perpetual contracts

QQQ and SPY may be used for market intelligence only, not direct execution.

### 4. Build Slowly

The project starts manually before automation.

No complex feature should be added until the previous stage is working cleanly.

### 5. Keep the System Simple

The system should produce clear actions:

- BUY
- HOLD
- WAIT
- SKIP
- REDUCE
- EXIT
- LOCK

No alert should confuse the user.

---

## Capital Plan

### Starting Structure

- Starting capital: £100
- Monthly addition: £100
- No principal withdrawals initially
- First objective: survival and system validation

### Two-Year View

Approximate total contributed capital after 24 months:

```text
£100 initial capital + £100 monthly additions = approximately £2,500 contributed capital
```

The early phase is not about aggressive returns.

The early phase is about:

- clean data
- discipline
- avoiding large losses
- understanding which setups work
- building confidence in the system

---

## Dual Engine Structure

## Engine A — Long-Term Halal ETF Compound Engine

### Purpose

This engine is designed for:

- long-term wealth building
- lower stress investing
- monthly capital deployment
- portfolio compounding
- controlled rebalancing

### Actions

- BUY
- HOLD
- REBALANCE
- REDUCE
- EXIT

### Core Logic

```text
IF asset remains halal-approved
AND long-term thesis is valid
AND portfolio risk is acceptable
    → HOLD or BUY

IF asset becomes over-allocated
OR sector risk increases
OR drawdown reaches review level
    → REDUCE or REBALANCE

IF long-term invalidation is confirmed
    → EXIT
```

---

## Engine B — Gap Opportunity Engine

### Purpose

This engine is designed for:

- short-term tactical opportunities
- market open gap analysis
- continuation setup tracking
- statistical edge building
- behaviour control

### Actions

- BUY
- WAIT
- SKIP
- EXIT
- LOCK

### Core Logic

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

## Recommended Stack

| Layer | Tool |
|---|---|
| Alerts | TradingView |
| Backend | Google Apps Script |
| Database | Google Sheets |
| Notifications | Telegram |
| Analytics | Power BI later |
| Version Control | GitHub |
| Development | Codex |

---

## System Flow

```text
Market Opens
      ↓
Gap Detected
      ↓
TradingView Alert
      ↓
Webhook to Apps Script
      ↓
Risk + Market Rules Checked
      ↓
BUY / WAIT / SKIP / EXIT / LOCK
      ↓
Telegram Alert
      ↓
Trade Logged
      ↓
Analytics Updated
```

---

## Risk Rules

## Maximum Risk

Initial risk should remain small.

```text
Risk per trade: 1%–2% maximum
```

The system should avoid large account damage while the dataset is still small.

---

## Daily Rules

- 3 losing trades → trading lock
- daily drawdown limit must be respected
- no revenge trading
- no forced trades
- no late-session chasing without separate confirmation
- no entries outside the allowed trade window unless flagged for review
- cooldown periods must be applied after poor execution

---

## Weekly Rules

- reduce risk after poor discipline
- review behaviour log
- check whether rules were followed
- paper trade after repeated mistakes
- do not increase position size after emotional trades

---

## ETF Allocation Structure

Suggested starting split:

| Layer | Allocation |
|---|---|
| Long-Term Halal ETF Layer | 70%–80% |
| Gap Strategy Layer | 20%–30% |

The gap layer should remain smaller until enough real data exists.

---

## Data Tables

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

---

## Trade Window Rules

The Gap Opportunity Engine must include time-based execution rules.

### Purpose

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

---

## Alert System

Alerts must not be simple buy or sell messages.

Each alert should explain:

- what happened
- what asset is affected
- whether the alert is for the long-term ETF engine or the gap engine
- the current risk level
- the active trade window
- the setup expiry time
- the suggested action
- the reason behind the action
- the maximum allowed position size
- the stop-loss or invalidation level
- whether the trade is allowed, delayed, reduced, or blocked
- what to review next

---

## Simple Alert Language Standard

Alerts should be readable on a mobile screen.

They should avoid overly technical language.

Each alert should answer:

```text
What happened?
Can I act now?
How much can I risk?
What would cancel the trade?
When does the setup expire?
What should I do next?
```

---

## Build Stages

## Stage 1 — Manual Tracker

Build:

- Google Sheet tracker
- asset watchlist
- trade journal
- behaviour log
- portfolio log

Success condition:

```text
A trade can be manually recorded from signal to exit.
```

---

## Stage 2 — Gap Detection Rules

Build:

- TradingView watchlist
- gap detection logic
- trade window detection
- session phase tagging

Success condition:

```text
The system can identify and classify a gap setup.
```

---

## Stage 3 — Apps Script Webhook

Build:

- webhook endpoint
- alert receiver
- signal logger
- error handler

Success condition:

```text
TradingView can send an alert into Google Sheets.
```

---

## Stage 4 — Telegram Alerts

Build:

- Telegram bot connection
- simple mobile alert format
- detailed alert format
- error alert format

Success condition:

```text
A valid signal creates a readable Telegram alert.
```

---

## Stage 5 — Risk Engine

Build:

- account risk calculator
- daily loss limit
- trade lock
- time-window risk lock
- setup expiry rules

Success condition:

```text
The system can block trades when risk rules fail.
```

---

## Stage 6 — Halal Asset Filter

Build:

- halal status field
- approved asset list
- blocked asset logic
- reference-only asset logic

Success condition:

```text
The system can separate market intelligence assets from execution assets.
```

---

## Stage 7 — Portfolio Monitor

Build:

- long-term holdings tracker
- drawdown monitor
- rebalance alerts
- reduce exposure alerts

Success condition:

```text
The system can monitor long-term holdings and suggest controlled action.
```

---

## Stage 8 — Analytics Dashboard

Build:

- signal performance view
- trade performance view
- win/loss tracking
- setup quality review
- rule-following score

Success condition:

```text
The system shows which setups are working and which are failing.
```

---

## Stage 9 — Behaviour Engine

Build:

- FOMO tracking
- revenge trade tracking
- late-entry tracking
- skipped valid setup tracking
- time-of-day behaviour review

Success condition:

```text
The system can identify user behaviour patterns that damage performance.
```

---

## Stage 10 — Power BI Dashboard

Build:

- performance dashboard
- portfolio dashboard
- behaviour dashboard
- risk dashboard
- monthly review report

Success condition:

```text
The system can support long-term decision making with visual analytics.
```

---

## Codex Rules

Codex must follow these rules:

- do not skip stages
- no leverage features
- no hardcoded API keys
- every stage must be testable
- keep architecture modular
- protect capital first
- keep user-facing alerts simple
- do not build execution automation before journaling and risk logic are stable
- do not add broker execution without explicit future approval
- every new feature must include a test case or manual test instruction

---

## Definition of Success

## Month 1

Success means:

- functioning tracker
- clean data
- no major losses
- all gap signals logged
- trade window timestamps recorded
- behaviour mistakes tracked
- no emotional scaling

---

## Month 6

Success means:

- consistent execution
- growing dataset
- controlled behaviour
- risk rules followed
- basic analytics available
- clear understanding of which setups perform best

---

## Year 2

Success means:

- scalable framework
- strong discipline
- measurable edge
- meaningful capital base
- mature long-term halal portfolio
- evidence-backed tactical strategy

---

## Final Philosophy

The system is not designed to predict everything.

It is designed to:

- protect capital
- avoid emotional decisions
- identify higher-quality opportunities
- build evidence
- scale slowly and intelligently

The most powerful system decisions are often:

- SKIP
- WAIT

BUY should only happen when:

- market conditions
- risk conditions
- halal rules
- trade window rules
- historical probabilities align
