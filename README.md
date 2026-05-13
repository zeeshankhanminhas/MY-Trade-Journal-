# MY-Trade-Journal

A clean trading operating system for halal-conscious investing, gap opportunities, risk control, and trade journaling.

This project is designed to help build discipline, protect capital, track trading behaviour, and slowly develop a data-backed edge.

---

## What This Project Is

MY-Trade-Journal is a controlled personal trading and investing system built around two parallel engines:

1. **Long-Term Halal ETF Compound Engine**
2. **Gap Opportunity Engine**

The system is not designed to predict every market move.

It is designed to help decide when to:

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

Automation will be added gradually using TradingView, Google Apps Script, Google Sheets, Telegram, and later Power BI.

---

## System Overview

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

## Documentation

| Document | Purpose |
|---|---|
| [Core Master Framework](docs/CORE_MASTER_FRAMEWORK.md) | Project philosophy, capital plan, and operating principles |
| [Gap Opportunity Engine](docs/GAP_ENGINE.md) | Gap setup rules, trade windows, session phases, and expiry logic |
| [Long-Term Halal ETF Compound Engine](docs/ETF_COMPOUND_ENGINE.md) | Long-term ETF allocation, portfolio monitoring, and rebalancing logic |
| [Risk Rules](docs/RISK_RULES.md) | Daily, weekly, lock, and capital protection rules |
| [Data Schema](docs/DATA_SCHEMA.md) | Required Google Sheets tables and fields |
| [Alert System](docs/ALERT_SYSTEM.md) | Mobile-friendly alert structure and action language |
| [Build Stages](docs/BUILD_STAGES.md) | Stage-by-stage roadmap from manual tracker to dashboard |
| [Codex Rules](docs/CODEX_RULES.md) | Build rules Codex must follow when adding features |
| [Disclaimer](docs/DISCLAIMER.md) | Personal-use and financial-risk disclaimer |

---

## Build Order

The project should be built in this order:

```text
Manual logging
→ signal detection
→ webhook receiver
→ Telegram alerts
→ risk engine
→ halal asset filter
→ portfolio monitor
→ analytics dashboard
→ behaviour engine
→ Power BI dashboard
```

Do not skip stages.

---

## Core Actions

The system should produce clear actions only:

- BUY
- HOLD
- WAIT
- SKIP
- REDUCE
- EXIT
- LOCK

No alert should confuse the user.

---

## Disclaimer

This project is for personal tracking, journaling, research, and system discipline only.

It is not financial advice, investment advice, halal financial advice, tax advice, or a recommendation to buy or sell any asset.

All trading and investing decisions remain the responsibility of the user.

See: [Disclaimer](docs/DISCLAIMER.md)
