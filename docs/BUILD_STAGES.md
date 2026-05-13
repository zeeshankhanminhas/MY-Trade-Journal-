# Build Stages

MY-Trade-Journal must be built stage by stage.

Do not skip stages.

---

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
