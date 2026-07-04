# Artifact Curation Lifecycle

**Diagram type:** state — traces every artifact through the curation pipeline from creation to final disposition. This is the state machine that governs all intern-produced artifacts in the program.

Each artifact moves through exactly this lifecycle. The curation decisions (Merge, Revise, Defer, Discard) are made by research professionals during twice-weekly batch reviews. Interns continue producing new artifacts during the 3-4 day gap between reviews. For the full curation policy, see [`INTERNSHIP_SPECIFICATION.md`](../../Internship/INTERNSHIP_SPECIFICATION.md) §9.

```mermaid
stateDiagram-v2
    [*] --> Draft : Intern begins

    Draft --> Submitted : Intern commits & pushes
    Draft --> Draft : Intern revises locally

    Submitted --> InReview : RP picks up for batch review

    state InReview {
        [*] --> Evaluating
        Evaluating --> Deciding : RP reaches decision

        state Deciding {
            [*] --> Merge_decision
            [*] --> Revise_decision
            [*] --> Defer_decision
            [*] --> Discard_decision
        }
    }

    InReview --> Merged : Merge — accepted as-is
    InReview --> Revising : Revise — specific feedback given
    InReview --> Deferred : Defer — hold for dependencies
    InReview --> Discarded : Discard — out of scope or superseded

    Revising --> Submitted : Intern addresses feedback, re-commits

    Deferred --> Submitted : Dependencies met, resubmit

    Merged --> [*] : Artifact in collection
    Discarded --> [*] : Archived / removed

    note left of Draft : Artifact begins here.\nEvery research session\nmust produce a commit.
    note right of InReview : Twice-weekly batch review.\n3-4 day max latency.
    note left of Revising : Intern sees specific\nactionable feedback via\nGitHub review comments.
```

**Cross-references:**
- [`INTERNSHIP_SPECIFICATION.md`](../../Internship/INTERNSHIP_SPECIFICATION.md) §9 — Curation decision gradient and cadence
- [`PROSPECTIVE_INTERN_GUIDE.md`](../../Internship/PROSPECTIVE_INTERN_GUIDE.md) §"The Cadence" — How curation fits into weekly rhythm
- [`ONBOARDING_CHECKLIST.md`](../../Internship/ONBOARDING_CHECKLIST.md) — First curation review happens Week 2
