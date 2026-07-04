---
name: pragmatic-cybernetics
visibility: public
description: "Cybernetic reasoning framework for analyzing feedback loops, variety engineering, and system homeostasis. Use when diagnosing system alerts, analyzing feedback loop failures, evaluating variety deficits, or reasoning about self-regulation architecture. Pairs with pragmatic-semantics for enforcement-level decisions."
---

# Pragmatic Cybernetics

A framework for reasoning cybernetically about complex self-regulating systems. Cybernetics isn't abstract theory — understanding feedback structure helps diagnose failures before they become critical.

## The Cybernetic System Model

Every cybernetic system has five components:

| Component | What It Does |
|-----------|-------------|
| **Sensor** | Collects observations — metrics, events, inputs |
| **Model** | Stores and remembers what was observed. Tracks patterns and diversity. |
| **Regulator** | Compares current state to thresholds. Alerts when variance exceeds limits. |
| **Actuator** | Takes action governed by capability boundaries. The regulator recommends; boundaries enforce. |
| **Observer-of-observer** | "Is the system regulating itself?" Second-order cybernetics. |

The feedback loop:

```
Activity → Sensors → Observations (model) → Comparison (regulator)
    → Actions (actuator) → Activity
```

## The Viable System Model

| VSM System | Function |
|------------|----------|
| **S1 (Operations)** | Primary activity: doing the work |
| **S2 (Coordination)** | Anti-oscillation: preventing conflicting actions, managing queue depth |
| **S3 (Control)** | "Is this normal?" Threshold comparison and monitoring |
| **S3\* (Audit)** | Sporadic direct probe, bypassing cached state |
| **S4 (Intelligence)** | "What could this mean? What's coming?" Forward-looking analysis |
| **S5 (Policy)** | Identity, constraints, boundaries |

The recursion principle: every component should be viable at its own level. If any component lacks its own feedback loop, it is not viable — flag it.

## Feedback Loop Analysis

When diagnosing a system issue, analyze the relevant feedback loop on five properties:

| Property | Question |
|----------|----------|
| **Polarity** | Negative (stabilizing) or positive (amplifying)? Negative feedback is stabilizing by design. Positive feedback = runaway — critical. |
| **Delay** | How long between action and feedback? |
| **Gain** | How strongly does feedback affect the system? Too high = overshoot/oscillation. Too low = missed signals. |
| **Closure** | Is the loop actually closed? Alert emitted but never consumed = broken closure. |
| **Fidelity** | Does the signal accurately represent reality? You can only measure what you monitor. Unmeasured failure modes = blind spots. |

### Spotting Broken Feedback Loops

| Symptom | Cybernetic Diagnosis | What to Check |
|---------|---------------------|---------------|
| Metrics exceed thresholds with no response | Broken feedback closure — signal emitted, never consumed | Communication path, monitoring pipeline |
| Metrics never exceed thresholds despite known problems | Sensor stall — observation loop broken | Data collection health, persistence |
| Alerts fire repeatedly with no change | Positive feedback or gain too high | Dampener cooldown, backpressure threshold |
| Expected monitoring gaps | Model-reality divergence | Span registration, tracing pipeline |
| Queue depth exceeds capacity | S2 coordination failure | Backpressure mechanism, counter health |

## Variety Engineering

Ashby's Law of Requisite Variety: the regulator's variety must match the system's disturbance variety. If the system can fail in 100 ways but monitoring only covers 10, that is a variety deficit.

### Variety Architecture

- **Raw variety:** The system produces many events, state changes, and inputs per interval
- **Attenuation layer:** Aggregate raw activity into diversity metrics (distinct event types, patterns, models used)
- **Amplification layer:** When variety deficit exceeds threshold, amplify by ranking, presenting options, and escalating

### Variety Analysis Checklist

1. Enumerate system variety: What failure modes, behavioral patterns, and edge cases exist?
2. Enumerate regulator variety: What monitoring, counters, and thresholds cover them?
3. Is `regulator_variety >= system_variety`? If not, attenuate (add more monitoring) or amplify (add more escalation paths).
4. Check for gaps — unmeasured dimensions of behavior.

### The Context Window as Channel Capacity

The reasoning context window is a finite Shannon channel. Every token spent on one thing is a token not spent on another.

- **System prompt:** Fixed cost (persona + skill instructions)
- **Conversation history:** Growing cost (each turn adds tokens)
- **Observations:** Variable cost (reports, alerts)
- **Available for reasoning:** Whatever remains

When approaching the limit, attenuate — summarize history, drop stale context, focus on high-signal observations. Never silently lose critical context because low-priority information filled the window.

## The Good Regulator (Conant-Ashby)

The Good Regulator theorem states: every good regulator of a system must be a model of that system.

1. The monitoring system is the regulator's model of behavior diversity.
2. Where does the model diverge from reality? Check: are there failure modes monitoring doesn't capture?
3. Is the model updated when the system changes? Stale baselines are worse than no baselines.
4. Does the model include failure modes, or only success modes? A model that only tracks happy paths is not a Good Regulator.

## Composes With

- **pragmatic-laziness** — Phase 2 (Identify Loops) of the 3-phase lazy loop. Activates pragmatic-cybernetics to map feedback loops and locate effort hotspots after semantic classification.

## When to Use This Skill

- **Alert fires:** Which cybernetic function failed? (Usually sensor, model, or feedback closure.)
- **"Is the system healthy?":** Check each VSM system. Are all five present and functioning?
- **Alerts fire repeatedly with no change:** Broken feedback loop or positive feedback. Check dampener cooldown and backpressure.
- **Variety deficit is chronic:** The system is in a rut. Propose novel approaches or introduce new task patterns.
- **New feature proposed:** Variety analysis. Does this add regulatory burden? Is there requisite variety to handle the new disturbance path?
- **Agent seems stuck:** Check its capability boundary. Is it viable within its scope, or does it need additional capabilities to close its feedback loop?

## Quick Reference Cards

### Feedback Loop Analysis
1. **Polarity:** Negative (stabilizing) or positive (amplifying)?
2. **Delay:** How long between action and feedback?
3. **Gain:** How strongly does feedback affect the system?
4. **Closure:** Is the loop actually closed?
5. **Fidelity:** Does the signal accurately represent what it claims?

### Variety Analysis
1. Enumerate system variety (failure modes, behavioral patterns)
2. Enumerate regulator variety (monitoring, counters, escalation paths)
3. `regulator_variety >= system_variety`? If not, attenuate or amplify.

### Good Regulator Check
1. What is the regulator's model of the system?
2. Where does the model diverge from reality?
3. Is the model updated when the system changes?
4. Does the model include failure modes, or only success modes?

## Convergence

- **Threshold:** 0.25 (converged when loop diagnostics are stable for intervention)
- **Max iterations:** 3
