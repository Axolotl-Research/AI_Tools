---
name: diataxis-diagram
description: "Generate Mermaid diagrams from code using Diataxis methodology. Three core types: ERD (from SQL), flowchart (from code paths), state (from enums/lifecycles). Two extended types: sequence (from message flows), class (from traits/structs). See https://diataxis.fr/ for the documentation framework and https://mermaid.js.org/ for diagram syntax."
---

# Diataxis Diagram

Generate Mermaid diagrams from code, anchored in the [Diataxis](https://diataxis.fr/) documentation framework and [Mermaid](https://mermaid.js.org/) diagram syntax. All diagrams render natively in Zed.

## Quick Start

```
diataxis-diagram erd                        # Database schema → ERD
diataxis-diagram flowchart <function>       # Code path → decision tree
diataxis-diagram state <enum_or_module>     # Lifecycle → state machine
diataxis-diagram sequence <message_flow>    # Message passing → sequence
diataxis-diagram class <trait_or_module>    # Type hierarchy → class diagram
```

Output goes to `docs/diagrams/{type}-{target}.md`. Each file includes a plain-English description above the Mermaid block so it's useful even when not rendered.

## Diagram Type Selection

Not everything is a flowchart. Use the right type for the job:

| If you're showing... | Use | Because |
|---|---|---|
| Database tables and relationships | **erd** | Crow's Foot notation shows cardinality directly |
| Decision trees, process flows, pipelines | **flowchart** | Branches and paths are first-class |
| Lifecycles, statuses, state transitions | **state** | States and transitions are the domain, not an overlay |
| Request/response chains, event propagation | **sequence** | Participants and message ordering are explicit |
| Trait hierarchies, struct composition | **class** | Inheritance and composition have dedicated syntax |

**Heuristic:** If you find yourself drawing boxes labeled with states and arrows labeled with triggers → use state. If you find yourself drawing arrows between services with messages on them → use sequence. If you find yourself drawing rectangles and diamonds → use flowchart.

---

## Core Diagram Types

### ERD — from SQL schemas

Reads `*.sql` files or inline SQL in Rust. Extracts tables, columns, primary keys, and foreign key references.

**Mermaid syntax reference:** https://mermaid.js.org/syntax/entityRelationshipDiagram.html

**Conventions:**
- Type annotations in columns: `TEXT wallet_id PK`, `INTEGER amount`
- FK columns marked with `FK` annotation
- Crow's Foot relationship notation: `||--o{` (one-to-many), `||--||` (one-to-one), `}o--o{` (many-to-many)
- `REFERENCES` without `UNIQUE` on the FK → one-to-many
- `REFERENCES` with `UNIQUE` on the FK → one-to-one
- Junction tables (two FK columns) → many-to-many through the junction
- Skip `CREATE VIRTUAL TABLE`, `INSERT` statements
- List notable indexes in a footnote table below the diagram, not in the Mermaid block

**Cardinality inference:**
```
wallet_balances ||--o{ wallet_transactions : "wallet_id"     # FK, no UNIQUE → one-to-many
human_users ||--|| consent_records : "webid"                 # FK with UNIQUE → one-to-one
orders }o--o{ products : "via order_items"                    # Junction table → many-to-many
```

### Flowchart — from code paths and decision logic

Reads Rust functions or service methods. Traces control flow: entry → branches → outcomes.

**Mermaid syntax reference:** https://mermaid.js.org/syntax/flowchart.html

**Conventions:**
- Use `flowchart TD` (top-down) for most diagrams; `LR` (left-right) only for wide pipelines
- Node labels ≤ 40 characters
- Node shapes by semantic role:
  - `A[rectangle]` — action or process step
  - `B{rhombus}` — decision or branch point
  - `C([rounded])` — start or end
  - `D[(cylinder)]` — data store or database
  - `E[[subroutine]]` — predefined process or external call
- Edge labels on decision branches: `-->|Yes|`, `-->|No|`
- Use `subgraph` to group related nodes when a flow spans multiple domains

**Extraction rules:**
- Function entry point → start node `([Start])`
- `if`/`match` expressions → decision nodes `{Decision?}`
- Function calls, template executions → action nodes `[Action]`
- `return`/`Ok`/exit → terminal nodes `([End])`
- Loop/while/for → loop-back edges with `-->|\"retry\"|`

### State — from enums and lifecycle code

Reads Rust enums with lifecycle semantics, state fields in structs, or transition methods. Traces all reachable states and their transitions.

**Mermaid syntax reference:** https://mermaid.js.org/syntax/stateDiagram.html

**Conventions:**
- `[*]` for start and end states
- Transition labels on arrows: `State1 --> State2 : trigger_name`
- `<<fork>>` for states that branch into parallel paths
- `<<join>>` for states where parallel paths converge
- `note left of State : description` for annotations and guard conditions
- Composite states with `state Name { ... }` for nested state machines

**Extraction rules:**
- Enum variants → states (e.g., `Pending`, `Active`, `Completed`, `Failed`)
- `match` arms in transition functions → transitions between states
- Guard conditions in match guards → annotated on transition labels or in notes
- Terminal variants (no outgoing transitions) → transitions to `[*]`
- `Default` impl or constructor → initial state `[*] --> InitialState`

---

## Extended Diagram Types

These are used less frequently but have dedicated Mermaid syntax when the core types don't fit.

### Sequence — from message passing and event chains

Reads handler code, event propagation traces, or service call chains.

**Mermaid syntax reference:** https://mermaid.js.org/syntax/sequenceDiagram.html

**Conventions:**
- Use `participant A as Full Name` for readable aliases
- `->>` for synchronous calls, `-->>` for async responses
- `+`/`-` for activation bars: `A->>+B: call`, `B-->>-A: response`
- Use block constructs for real-world flows:
  - `loop [description] ... end` for retry/repeat logic
  - `alt [case] ... else [other case] ... end` for branching
  - `opt [condition] ... end` for optional steps
  - `par ... and ... end` for parallel execution
- `Note over A,B: description` for cross-participant annotations

### Class — from trait hierarchies and struct composition

Reads Rust `trait` and `impl` blocks, and struct definitions.

**Mermaid syntax reference:** https://mermaid.js.org/syntax/classDiagram.html

**Conventions:**
- `<<interface>>` for traits
- `<<enumeration>>` for enums
- `+` public, `-` private for methods and fields
- `A <|-- B : implements` for trait implementation
- `A <|-- B : extends` for supertrait relationships
- `A o-- B : composes` for struct fields
- `A ..> B : uses` for function parameters and dependencies
- Multiplicity labels: `A "1" o-- "0..*" B`
- Group related types with `namespace Name { ... }`

---

## Diataxis Anchoring

Diagrams are a **medium**, not a quadrant. Each diagram serves a specific reader need based on where it appears in documentation:

| Diagram placed in... | Serves... | Reader is... | Diagram should... |
|---|---|---|---|
| **Reference** section | Information need | Practitioner consulting facts | Be austere, complete, faithfully mirror the code structure |
| **How-to** section | Action need | Practitioner executing a task | Show the path, omit alternatives, keep focused on the goal |
| **Explanation** section | Understanding need | Reader reflecting on design | Show relationships, context, trade-offs, alternatives |
| **Tutorial** section | Learning need | Student following a lesson | Be minimal, point out what to notice, avoid overwhelming detail |

**Voice per quadrant** (from [diataxis.fr](https://diataxis.fr/)):
- Tutorial diagrams: "We'll build this together" — concrete, step-by-step, minimal
- How-to diagrams: "To achieve X, follow this path" — direct, actionable, goal-focused
- Reference diagrams: "Here is the schema" — neutral, complete, descriptive only
- Explanation diagrams: "Here's why it works this way" — discursive, contextual, may show alternatives

This skill's default output is **reference-grade** (neutral, complete, code-anchored). When placing a diagram in a how-to or tutorial, adapt the accompanying prose — not the Mermaid source — to match the quadrant voice.

---

## Quality Gates

### For Every Diagram
- [ ] Entity/table/state/class count matches the source (no omissions)
- [ ] All relationships use the correct Mermaid syntax for their type
- [ ] Every relationship has the correct cardinality (one-to-one vs one-to-many vs implements vs extends)
- [ ] Node labels are ≤ 40 characters and use plain English (not raw identifiers)
- [ ] A plain-English description paragraph appears above the Mermaid block
- [ ] At least one cross-link to related documentation
- [ ] `flowchart TD` (top-down) is used unless the diagram is inherently wide (pipeline, timeline)

### Diataxis Quality (from https://diataxis.fr/quality/)
- **Functional quality:** Accurate, complete, consistent with the source code
- **Deep quality:** Flows naturally, fits the reader's need, anticipates what they'll look for next
- **List discipline:** Tables of contents, entity lists, and relationship lists use ≤ 7 items per group

---

## Output Conventions

- **Directory:** `docs/diagrams/` (create if missing)
- **File naming:** `{type}-{target-slug}.md` (e.g., `erd-schema.md`, `state-goal-lifecycle.md`)
- **Commit:** `docs: add {type} diagram for {target}`
- **Layout:** Prefer taller over wider — Zed's Mermaid renderer is narrow
- **No styling:** Zed auto-themes Mermaid. Do not use `%%{init}%%`, `classDef`, or inline styles
