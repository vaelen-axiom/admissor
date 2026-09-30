# No Hindsight First

**Research note — 30 September 2026**

A historical test becomes unreliable when information that did not exist at the decision boundary is allowed to influence the reconstructed decision.

AXIOM's current research contract is therefore organized around a separation between:

1. **What was known at T** — the evidence available at the historical decision boundary.
2. **The first failed gate** — the earliest required predicate that could not be satisfied.
3. **What was unavailable at T** — later observations explicitly excluded from the decision object.
4. **What happened afterward** — future-only outcome evidence, retained separately for evaluation.

## Why rejected states matter

A rejection is still an observation.

If a required condition such as `HTF_EXISTS` is false at the historical boundary, the research record should preserve that failure rather than manufacture a trade or infer a setup from later market behavior.

The intended reconstruction is:

```text
historical closed evidence <= T
        |
        v
decision-time predicates
        |
        +-- first failed gate --> rejected / no establishment
        |
        v
frozen determination

future observations > T
        |
        v
outcome evaluation only
```

This makes the question *"What did the system know before the outcome existed?"* prior to questions about returns, win rate, or other execution-derived performance metrics.

## Current evidence status

The current AXIOM research interface exposes this separation directly in its rejection investigation:

- decision-time evidence is identified independently from later observations;
- later candles are marked as unavailable at the historical boundary;
- the first failed predicate and other unsatisfied conditions are retained;
- subsequent outcome information is presented as future-only evidence.

This is **evidence of the visible reconstruction contract**, not by itself proof that every implementation path is free from temporal leakage.

## Verification still required

Before making a stronger leakage-free claim, the implementation should be tested across instruments, timeframes, data boundaries, and replay/backtest paths to verify that future information cannot enter decision-time state.

Until then, the claim remains deliberately narrower:

> **No hindsight first. Performance claims later.**

---

Part of the ADMISSOR / AXIOM public evidence trail.
