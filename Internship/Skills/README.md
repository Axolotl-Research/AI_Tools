# Skills Collection — User Guide

This is the Axolotl Research skills library — 16 agent skills that extend what your AI tools (Cline, KiloCode, Zed Agent) can do. Each skill is a set of instructions that teaches the agent a specific thinking pattern, methodology, or workflow.

**How skills work:** You invoke a skill by name — the agent loads its instructions and follows them. Skills don't require installation. They are plain text files that the agent reads and applies. Some skills compose with others (e.g., `pragmatic-laziness` activates `essentialist` and `grill-me` internally).

---

## Quick Reference

| If you need to... | Use |
|-------------------|-----|
| Simplify a design or delete unnecessary code | [`essentialist`](#essentialist) |
| Stress-test a plan or design with hard questions | [`grill-me`](#grill-me) |
| Make text shorter / denser | [`caveman`](#caveman) |
| Frame a research question into a testable hypothesis | [`hypothesis-framer`](#hypothesis-framer) |
| Make a calibrated probability forecast | [`superforecasting`](#superforecasting) |
| Extract structured data from prose or documents | [`structured-extraction`](#structured-extraction) |
| Learn scientific thinking (PDCA, facts vs. interpretations) | [`kata-starter`](#kata-starter) |
| Achieve a measurable goal through rapid experiments | [`kata-improvement`](#kata-improvement) |
| Coach someone through scientific problem-solving | [`kata-coaching`](#kata-coaching) |
| Communicate constructively without negating | [`improv`](#improv) |
| Classify statements by how certain you should be | [`pragmatic-semantics`](#pragmatic-semantics) |
| Diagnose why a system isn't self-correcting | [`pragmatic-cybernetics`](#pragmatic-cybernetics) |
| Find the simplest possible approach to a problem | [`pragmatic-laziness`](#pragmatic-laziness) |
| Compose multiple skills into a coordinated bundle | [`skill-bundler`](#skill-bundler) |
| Generate diagrams from code or structures | [`diataxis-diagram`](#diataxis-diagram) |
| Get a higher-level map of unfamiliar code | [`zoom-out`](#zoom-out) |

---

## Thinking & Reasoning

### pragmatic-semantics

**What it does:** Teaches the agent to classify every statement along three axes: IS vs. OUGHT (descriptive vs. prescriptive), how certain (declarative / probabilistic / subjunctive), and which domain it anchors to. When you ask "how do you know that?" the agent traces provenance — was this directly measured, inferred, inherited from a baseline, or just an LLM guess?

**When to use:** Any time you want to know *how much to trust* what the agent is telling you. Especially useful when the agent makes claims about facts — ask it to run `pragmatic-semantics` on its own output. The agent will tag each claim with its epistemic mode and confidence level.

**Key concept:** The constraint hierarchy — Prohibitions (never violable) > Guardrails (only overridable with explicit consent) > Guidelines (relaxable with reason) > Evidence > Hypothesis. This is the foundation for several other skills.

---

### pragmatic-cybernetics

**What it does:** Teaches the agent to think in feedback loops. Borrows from cybernetics (the science of self-regulating systems): sensors, models, regulators, actuators, and second-order observation. When something isn't working, the agent diagnoses *which part of the feedback loop is broken* — is the sensor stale? Is the regulator's model wrong? Is the loop not closed?

**When to use:** When a process keeps failing in the same way, when metrics don't match reality, or when you need to understand why a system isn't self-correcting. Also useful for understanding Ashby's Law of Requisite Variety — the regulator must be at least as varied as the system it regulates.

**Internship connection:** Your research cycle is a cybernetic feedback loop. You prompt (actuator) → the AI responds (sensor) → you verify and synthesize (model/regulator) → you commit (new state). When your research stalls, cybernetic diagnosis tells you *which part of the loop* needs attention.

---

### pragmatic-laziness

**What it does:** A meta-skill that composes `pragmatic-semantics`, `pragmatic-cybernetics`, `essentialist`, and `grill-me` into a three-phase "lazy loop": (1) Decompose the problem into syntax/semantics/pragmatics, (2) Identify the feedback loops driving the work, (3) Find the path of least total action — what can be deleted without losing behavior? The governing principle: *the universe is lazy; be lazier.*

**When to use:** Before building anything substantial. When a design feels heavy or over-engineered. When two approaches conflict and you need to find the simplest viable path.

**Key insight:** The brachistochrone rule — the laziest path isn't always obvious. Sometimes you must go *through* apparent complexity to extract the deeper pattern that ultimately reduces total system action.

---

## Simplification & Quality

### essentialist

**What it does:** A recursive eliminative interrogation. Everything is assumed guilty until proven necessary through three gates: **Exist** (if I delete this, does any behavior vanish?), **Surface** (are there more than 7 public items? justify each extra), **Contract** (can I replace this abstraction with a direct call?). Pass all three gates, narrow scope, repeat. Zero deltas on second pass = done.

**When to use:** "Simplify this." "What can be deleted?" "Audit this for complexity." "Strip this module." Any time you want to reduce something to its essential core. Runs in advisory mode (shows you findings, you approve) or autonomous mode (reduces and loops without pause).

**Internship connection:** Run this on your framework before submitting for curation. It will force you to justify every entity in your ER diagram, every section in your capstone, every abstraction in your code.

---

### caveman

**What it does:** Two compression modes in one skill. **Caveman mode** strips stylistic filler — drops articles, hedging, pleasantries — while preserving all technical substance. **Dense mode** (Chain-of-Density) iteratively packs more entities into fixed-length text. **Combined mode** (dense → caveman) gives maximum information in minimum prose.

**When to use:** "Make this terse." "Summarize this densely." "TL;DR." Token budget tight. Useful when feeding long documents as context to an AI agent and you need to maximize information density.

**What NOT to compress:** Code blocks, error messages, URLs, security warnings, beginner-facing explanations.

---

## Research & Forecasting

### hypothesis-framer

**What it does:** Takes a broad research interest and refines it through FINER criteria (Feasible, Interesting, Novel, Ethical, Relevant) and PICO framework (Population, Intervention, Comparison, Outcome). Produces a structured research question, a testable hypothesis with null hypothesis, and aligned research aims. Four-step PDCA cycle with convergence check.

**When to use:** "I have a research idea but don't know how to frame it." "Is my research question any good?" "Help me write a hypothesis." "I need study aims." Particularly useful at the start of your internship when narrowing your domain focus into a researchable question.

**Internship connection:** Before you start collecting entities, frame your domain as a research question. Hypothesis-framer forces you to define scope, specify what you're measuring, and identify what success looks like.

---

### superforecasting

**What it does:** An 8-stage calibrated probability forecasting pipeline following Tetlock's Good Judgment Project methodology: (0) Triage — is this worth forecasting? (1) Fermi decomposition — break into sub-questions. (2) Outside view — what's the base rate? (3) Inside view — what makes this case different? (4) Bayesian update — incorporate new evidence. (5) Dragonfly-eye synthesis — integrate multiple perspectives. (6) Calibration — use the full 0–100% scale. (7) Record — create a structured forecast record for later Brier scoring.

**When to use:** "Forecast this." "What's the probability of...?" "How likely is X to happen by Y?" Any time you need a probability estimate you can later check against reality.

**Internship connection:** Domain B (RWA tokenization) involves forecasting regulatory evolution, market adoption, and platform competition. Domain A (fermented foods and health) involves forecasting research directions and health claim approvals. Both benefit from calibrated, trackable predictions.

---

### structured-extraction

**What it does:** A three-stage pipeline that extracts structured data from unstructured text: (1) Identify entities against a target JSON schema, (2) Extract relations as subject-predicate-object triples, (3) Map to schema with field-level coverage reporting (extracted / inferred / unresolved). Give it a JSON schema and a block of text — it populates the schema and tells you what it couldn't find.

**When to use:** "Extract all companies, their revenue, and CEO from this article." "Populate this schema from that PDF." "What entities are in this document?" Useful for turning research reading into structured data for your domain framework.

**Internship connection:** Feed a research paper about fermentation microbiology to structured-extraction with a schema for organisms, metabolites, and health outcomes. The output becomes a row in your entity database.

---

## Scientific Thinking (Toyota Kata)

These three skills form a progression. Start with kata-starter, graduate to kata-improvement, add kata-coaching when you have a coach.

### kata-starter

**What it does:** Three deliberate practice routines for building scientific thinking habits: (1) **Five Questions Drill** — practice asking the five Coaching Kata questions in sequence until automatic. (2) **PDCA Cycle** — practice Plan-Do-Check-Act on a trivial process (like making coffee faster). (3) **Observation Drill** — practice distinguishing facts from interpretations.

**When to use:** When you're new to scientific thinking methods. When you keep jumping to solutions without testing. When you confuse what you think with what you measured. 20 minutes a day is better than 2 hours once a week.

**Internship connection:** The research cycle (prompt → synthesize → document → commit → curate) IS a PDCA cycle. Starter Kata installs the neural pathway for this pattern before you apply it to real domain research.

---

### kata-improvement

**What it does:** The 4-step scientific pattern for achieving challenging goals: (1) Understand the Direction — what capability gap from above? (2) Grasp the Current Condition — go and see, measure, don't assume. (3) Establish the Next Target Condition — measurable, 1 week to 3 months out, beyond current knowledge. (4) Iterate — rapid PDCA experiments, one obstacle at a time.

**When to use:** When a specific, measurable capability gap exists. Prerequisite: complete kata-starter first. Pairs with kata-coaching.

**Internship connection:** The 8-week program itself IS an Improvement Kata. The challenge comes from the specification. Your current condition is your domain knowledge at Week 1. Your target condition is the capstone deliverable surviving grill-me. The weekly research cycles are PDCA experiments.

---

### kata-coaching

**What it does:** The 5-question dialogue for teaching scientific thinking. The coach asks (in strict order): (1) What is the target condition? (2) What is the actual condition now? (3) What obstacles? Which ONE? (4) What is your next step? What do you expect? (5) How quickly can we go and see? The coach NEVER gives solutions — only asks questions that make the learner's thinking visible.

**When to use:** When you have a coach and an active Improvement Kata cycle. When the learner has explicitly consented to coaching. Daily, at the gemba (where the work happens), ~20 minutes.

**Internship connection:** Your research professionals (Ivan, Mario, Matt, Mike) function as coaches during curation. The curation review process mirrors the Coaching Kata — they identify gaps (Q3), give actionable feedback (Q4), and expect you to return with results (Q5).

---

## Interaction & Composition

### improv

**What it does:** Five constructive-by-default communication modes: **Plussing** — extract what's good, silently discard the rest, build on it. **Yes And** — accept the whole contribution and extend it. **Yes But** — accept and add a constraining boundary. **Freestyling** — time-bounded rapid collaborative cycling. **Riffing** — solo deep exploration from a seed idea, then return to group.

**When to use:** When collaborating with AI agents in brainstorming or design sessions. When you want to critique constructively without negating. When you need to explore ideas divergently before converging. Modes compose recursively (e.g., Plussing → Riffing: filter for the best seed, then explore it deeply).

**Core rule:** Never explicitly negate. Criticism is deletion-by-omission. Build on what works, silently discard what doesn't.

---

### skill-bundler

**What it does:** Composes multiple skills into a goal-anchored bundle. Extracts a structured goal from your intent, selects and orders skills to achieve it, validates for conflicts (divergent + convergent in same phase = conflict), and produces a manifest with cascade order, phase assignments, and convergence criteria.

**When to use:** "Bundle skills [skill-a, skill-b, skill-c]." "Compose these into a workflow." When you want multiple skills active in sequence during a single session.

**Pre-built bundles:**
- **self-review:** grill-me + essentialist → critically examine and simplify a design
- **kata-cycle:** kata-starter → kata-improvement → kata-coaching → build thinking and achieve a goal
- **forecast-and-test:** superforecasting + structured-extraction → make and record calibrated predictions
- **self-improvement:** pragmatic-laziness → essentialist → grill-me → reduce system action iteratively
- **research-design:** hypothesis-framer + superforecasting → frame a question and forecast outcomes

---

## Documentation & Design

### diataxis-diagram

**What it does:** Generates Mermaid diagrams from code or structures. Five diagram types: ERD (from SQL schemas), flowchart (from code paths), state (from enums/lifecycles), sequence (from message flows), class (from trait hierarchies). Output goes to `docs/diagrams/{type}-{target}.md` with a plain-English description above each diagram.

**When to use:** "Diagram this schema." "Flowchart this function." "State machine for this enum." When you need a visual map of structure, process, or state.

**Internship connection:** Your capstone deliverable requires ER diagrams of your domain framework. This skill generates them from your entity descriptions rather than you drawing them manually. It was used to create the diagrams in `docs/diagrams/`.

---

### zoom-out

**What it does:** Goes up a layer of abstraction. Produces a module map, caller graph, data flow trace, boundary summary, and key invariants for unfamiliar code — all using the project's own domain vocabulary.

**When to use:** When you're dropped into unfamiliar code and need to understand how it fits into the bigger picture. When you're lost in the weeds and need the 30,000-foot view.

**Internship connection:** When reading library code or exploring AI tool internals, use zoom-out to understand the architecture before diving into implementation details.

---

## Challenge & Interrogation

### grill-me

**What it does:** A relentless Socratic interview that stress-tests a plan, design, or argument. Asks escalating questions from Level 1 (Recall: "Can you define the term?") through Level 5 (Synthesis: "Can you redesign it for a novel scenario?"). Identifies weak points, hidden assumptions, and gaps.

**When to use:** Before submitting your capstone for final review. Before presenting your framework to Ivan. Whenever you think you understand something and want to test whether you really do. This is the quality bar for the entire internship program.

**Internship connection:** The capstone deliverable must survive grill-me interrogation. Use this skill *before* your final review — it will find the gaps so you can fill them. Use it throughout Weeks 6-8 during the Synthesis and Polish phases.

---

## Skill Progression for Interns

### Week 1-2 (Onboard / Learn)
- **kata-starter** — Install the PDCA pattern and fact-vs-interpretation distinction
- **zoom-out** — When exploring the library or AI tool internals
- **caveman** — When feeding long documents as context to AI agents

### Weeks 3-4 (Research-I — Entity Collection)
- **hypothesis-framer** — Frame your domain as a researchable question
- **structured-extraction** — Extract entities and relations from research papers
- **pragmatic-semantics** — When verifying claims from AI tools (trace provenance)

### Weeks 5-6 (Research-II — Relationship Mapping)
- **diataxis-diagram** — Generate ER diagrams from your entity collections
- **superforecasting** — Forecast domain evolution for temporal analysis
- **improv** — Constructive collaboration modes for brainstorming with AI

### Weeks 6-8 (Synthesis / Polish)
- **grill-me** — Self-test your framework before final review
- **essentialist** — Strip your capstone to its essential core
- **pragmatic-laziness** — Find and eliminate unnecessary complexity
- **skill-bundler** — Compose multiple review skills into a self-review pipeline

### Throughout (Research Professionals)
- **kata-coaching** — Research professionals use this posture during curation
- **pragmatic-cybernetics** — Diagnose when research cycles stall
- **improv (Plussing)** — Default constructive posture for all feedback

---

*Each skill lives in its own folder under `Skills/` with a `SKILL.md` file containing full instructions. Feed any SKILL.md to your AI agent as context when you want the agent to adopt that skill's methodology. Skills marked `composes_skills` internally activate other skills — you don't need to invoke them separately.*
