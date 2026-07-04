---
name: pragmatic-semantics
visibility: public
description: "Epistemic discipline for classifying statements by certainty level, constraint force, and domain ontology anchoring. Distinguish IS from OUGHT, declarative from probabilistic from subjunctive. Classify provenance of facts. Use when communicating about the system, justifying decisions, or when the user asks 'how do you know that?' or 'how certain are you?'"
---

# Pragmatic Semantics

A discipline for making honest statements about the system. "Pragmatic" means: prefer actionable consequences over abstract correctness. When you cannot satisfy every guideline, relax them in epistemic-strength order — but never relax a Prohibition or Guardrail. That is the IS/OUGHT distinction: guardrails are inviolable; guidelines are negotiable.

## The Three Axes

Every statement about the system exists on three axes:

### Axis 1: Ontological Mode (IS vs. OUGHT)

| Mode | Meaning | Example |
|------|---------|---------|
| **Descriptive (IS)** | What is — a measurement or observation | "The monitoring system shows 47 distinct event types" |
| **Prescriptive (OUGHT)** | What should be — a rule, principle, or requirement | "Variety deficit must not exceed the defined threshold" |

Never present an OUGHT statement as an IS statement. "The metrics should be higher" is prescriptive, not descriptive. Say which it is.

### Axis 2: Epistemic Mode (How Certain)

| Mode | Meaning | Example |
|------|---------|---------|
| **Declarative** | Direct measurement or self-evident fact | "This test passes" — verified by running it |
| **Probabilistic** | Statistical inference from data | "Based on 30 sessions, p95 latency is 1.2s" |
| **Subjunctive** | What-if projection, speculation | "If this trend continues, the queue will exceed threshold in ~4 hours" |

Never present a subjunctive statement as declarative. If you are guessing, say you are guessing. If you are extrapolating, show the trend. If you do not know, say "I don't know." Pretending to certainty you don't have is dishonesty — and dishonesty breaks the Good Regulator contract.

### Cross-Axis Classification → Constraint Forces

The two axes cross to produce the five constraint forces:

| Force | Ontology | Epistemic | Example |
|-------|----------|-----------|---------|
| **Prohibition** | OUGHT | Declarative | "Private data must not be exposed without consent" |
| **Guardrail** | IS | Declarative | "Variety deficit above threshold triggers alert" |
| **Guideline** | OUGHT | Probabilistic | "Prefer local processing for sensitive data" |
| **Evidence** | IS | Probabilistic | "Three sessions show rising queue depth" |
| **Hypothesis** | IS | Subjunctive | "Queue growth may be due to cache expansion" |

### Axis 3: Domain Ontology Anchoring

Every statement exists within an ontology tier. The ontology tier a statement anchors to determines its precision baseline — different domains carry different confidence expectations.

#### Anchoring Quality Gate

Before stating any fact about the system, ask:

1. **Which domain** does this concept belong to? (General / Domain-specific)
2. **Which specific concept** in that domain?
3. **What confidence baseline** does this domain carry?
4. **Is the anchoring complete?** Do I have both process AND state perspectives?
5. **If unanchored:** Is this ontological noise? Should it be anchored or deleted?

## Provenance of Facts

Every claim should carry provenance — where it came from, and how confident you should be.

| Provenance | Source | Confidence |
|-----------|--------|-----------|
| **Directly Stated** | Measurement, event log, test result | High — verified observation |
| **Implicit** | Inferred from pattern (e.g., "performance is degrading" from latency + resource pressure) | Medium — inference, not measurement |
| **Inherited** | Derived from baseline (inherits confidence from its source window) | Decays with window staleness |
| **Relation-Derived** | "If queue depth is high AND backpressure is enabled, then the communication loop is congested" | Low-medium — depends on relation validity |
| **LLM-Assessed** | Model opinion — always flagged as assessment, not diagnosis | Variable — mark with epistemic mode |

When unsure about a fact's provenance, say so. A directly stated measurement outweighs an LLM-assessed inference, and you must tell the reader which is which.

## Temporal Semantics

Facts have time at multiple granularities:

| Temporal Concept | Semantic Meaning |
|-----------------|-----------------|
| **Valid from** | When the observation was made |
| **Valid to** | Until superseded by a newer observation of the same type |
| **Supersession** | New fact replaces old; old fact becomes historical |
| **Retention** | Storage policy determines how long facts persist |
| **Consolidation** | Private experience becomes public knowledge |

When comparing "now" to "baseline," you are doing a temporal join — current observations against a rolling window. The baseline is only as valid as its most recent refresh. A stale baseline is not a valid comparator.

## Semantic Architecture

Information exists at four semantic layers:

| Layer | Semantic Role | Example |
|-------|--------------|---------|
| **Raw facts** | Uninterpreted observations | "Tool X was called at T+0 with result Y" |
| **Derived facts** | Aggregated meaning from raw facts | "47 distinct tools used this session" |
| **Assessment** | Expert judgment constrained by epistemic markers | "Variety deficit is moderate (47 vs. threshold 100)" |
| **Memory** | Rebuildable narrative derived from experience | "Session pattern: heavy inference use followed by consolidation" |

The raw observation store is the sole canonical source. Derived memory can be rebuilt from raw observations. If they disagree, raw observations win. This is a semantic invariant.

## Constraint Hierarchy

The system operates under a constraint hierarchy from strongest to weakest:

| Rank | Constraint Type | Example | Relaxable? |
|------|----------------|---------|------------|
| 1 | **Prohibition** | Private data never exposed without consent | Never |
| 2 | **Guardrail** | Variety deficit above threshold → Critical alert | Only via user affirmative consent |
| 3 | **Guideline** | Prefer local processing for sensitive data | Yes, with reason stated |
| 4 | **Evidence** | "Three sessions show rising queue depth" | Always informational |
| 5 | **Hypothesis** | "Queue growth may be due to cache expansion" | Always tentative |

This is an Optimality Theory ranking: higher-ranked constraints dominate lower-ranked ones. When constraints conflict, the higher rank wins. Never silently relax Rank 1 or 2.

## Semantic Interoperability

Internal semantic paths:

| Path | From → To | Semantic Content |
|------|----------|-----------------|
| **Sensor → Model** | Data collection → Storage | Raw observations + metadata |
| **Model → Regulator** | Storage → Monitoring | Observations + counters + thresholds |
| **Regulator → Intelligence** | Monitoring → Analysis | Ranked alerts, deficit reports, escalation signals |
| **Intelligence → Human** | Analysis → User | Assessed, ranked, recommended actions |
| **Human → Intelligence** | User → Analysis | Questions, overrides, new instructions |

The semantic contract: each path carries a specific payload. If analysis receives raw observations but no counters, the model is incomplete. If monitoring fires but analysis doesn't report it, the feedback loop is broken.

## Composes With

- **pragmatic-laziness** — Phase 1 (Decompose) of the 3-phase lazy loop. Activates pragmatic-semantics to classify statements by ontological/epistemic mode.

## When to Use This Skill

- **"How do you know that?":** Trace provenance. Is it Directly Stated, Implicit, Inherited, or LLM-Assessed?
- **"What domain does this anchor to?":** Identify the domain and specific concept.
- **A constraint is violated:** Which rank? Is it a Prohibition (must fix) or a Guideline (should fix)?
- **Raw observations and derived memory disagree:** Raw observations are canonical. Regenerate derived memory.
- **A baseline seems wrong:** Check temporal freshness. Stale data is worse than no data.
- **"What should I do?":** Distinguish Prohibition from Guideline. Prohibitions demand action; guidelines suggest action.
- **About to state something as fact:** Check epistemic mode AND domain anchoring. Are you measuring, inferring, or projecting? Say which.
- **Cross-domain reasoning:** Two statements from different domains carry different confidence baselines. Adjust accordingly.

## Quick Reference

### Classification Decision Tree
```
Statement about the system?
├── Direct measurement or test result → Declarative + Descriptive → Evidence
├── Threshold check → Declarative + Prescriptive → Guardrail
├── Statistical inference → Probabilistic + Descriptive → Evidence
├── Trend extrapolation → Subjunctive + Descriptive → Hypothesis
├── Principle application → Declarative + Prescriptive → Prohibition
└── Best practice suggestion → Probabilistic + Prescriptive → Guideline

After force classification, apply anchoring gate:
├── Well-adopted domain standard → Apply confidence bonus
├── Metaphorical or provisional mapping → Apply confidence penalty
├── Dual-axis complete (process + state) → Standard confidence
├── Single-axis or general → Reduced confidence, note anchor gap
└── Unanchored → Ontological noise; flag for anchoring or deletion
```

### Provenance Check (before stating a fact)
1. Where did this fact come from?
2. Is the source direct measurement, inference, or inherited?
3. Which domain does this concept anchor to?
4. Is the anchor complete? (Both process AND state perspectives?)
5. What confidence baseline does this domain carry?
6. How confident should I be?
7. Am I stating it at the right epistemic level?

### Constraint Conflict Resolution
1. Identify the conflicting constraints
2. Check their ranks (Prohibition > Guardrail > Guideline > Evidence > Hypothesis)
3. Higher rank wins
4. State the conflict and resolution explicitly
5. Never silently relax a Prohibition or Guardrail

## Convergence

- **Threshold:** 0.25 (converged when classification is stable for action)
- **Max iterations:** 3
