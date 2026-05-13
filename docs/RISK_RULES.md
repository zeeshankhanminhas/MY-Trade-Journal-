# Risk Rules

Risk control is the foundation of MY-Trade-Journal.

The system must protect capital before it seeks growth.

---

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

## Lock Conditions

The system should lock trading when:

- daily loss limit is reached
- 3 losing trades occur in one day
- revenge trading is detected
- repeated rule violations occur
- trade is attempted outside the allowed window without approval
- account risk exceeds the defined threshold

---

## Capital Protection Standard

The system should prefer:

- WAIT over forced entry
- SKIP over weak confirmation
- REDUCE over panic exit
- LOCK over emotional continuation
