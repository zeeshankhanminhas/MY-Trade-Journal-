# Codex Rules

Codex must follow these rules when building MY-Trade-Journal.

---

## Core Build Rules

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

## Development Standard

Every implementation should clearly state:

- files changed
- functions added
- manual test steps
- expected result
- known limitation

---

## Safety Standard

Codex must not introduce:

- automatic broker execution
- leverage
- margin trading
- CFD logic
- futures trading logic
- hidden API keys
- untested trade action logic

---

## Stage Discipline

Build order matters.

The project should move from:

```text
Manual logging → signal detection → webhook → alerting → risk engine → analytics
```

No later stage should be built before the earlier stage is usable.