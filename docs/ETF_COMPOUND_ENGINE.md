# Long-Term Halal ETF Compound Engine

The Long-Term Halal ETF Compound Engine is designed for lower-stress investing, monthly capital deployment, and controlled portfolio growth.

---

## Purpose

This engine is designed for:

- long-term wealth building
- lower stress investing
- monthly capital deployment
- portfolio compounding
- controlled rebalancing

---

## Actions

- BUY
- HOLD
- REBALANCE
- REDUCE
- EXIT

---

## ETF Allocation Structure

Suggested starting split:

| Layer | Allocation |
|---|---|
| Long-Term Halal ETF Layer | 70%–80% |
| Gap Strategy Layer | 20%–30% |

The gap layer should remain smaller until enough real data exists.

---

## Core Logic

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

## Portfolio Review Logic

The system should monitor:

- allocation percentage
- current value
- invested amount
- unrealised profit/loss
- drawdown from recent high
- risk status
- rebalance requirement
- next review date

---

## Controlled Action Standard

The engine should avoid panic selling.

Actions should be controlled:

- reduce exposure gradually
- rebalance only when rules require it
- avoid averaging down during rising volatility
- preserve long-term thesis unless invalidated
