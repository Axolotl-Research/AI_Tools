# Program Phase Transitions

**Diagram type:** state — shows the 8-week internship program as a state machine, with each phase's entry and exit criteria made explicit. Designed for the reference reader — someone consulting the program structure who needs to know what qualifies as completing each phase.

Each phase has a clear exit criterion (from [`INTERNSHIP_SPECIFICATION.md`](../../Internship/INTERNSHIP_SPECIFICATION.md) §8.2). Transitions are gated by these criteria, not by calendar date alone. The buffer phase is available at any point for interruptions. Compare with the Gantt timeline in the specification for the calendar view.

```mermaid
stateDiagram-v2
    [*] --> Onboard : Program start

    state Onboard {
        [*] --> Setup
        Setup --> FirstPush : GitHub push successful
        FirstPush --> FirstSession : Cline session completed
        FirstSession --> IntroPosted : WhatsApp intro posted
        IntroPosted --> LexiconStarted : Lexicon draft >= 10 terms
    }

    Onboard --> Learn : All 4 exit criteria met

    state Learn {
        [*] --> InitialPrompts
        InitialPrompts --> FirstArtifacts : 3+ artifacts committed
        FirstArtifacts --> FirstCuration : First curation review done
    }

    Learn --> ResearchI : First curation completed

    state ResearchI {
        [*] --> EntityCollection
        EntityCollection --> BatchReview : 5+ artifacts accumulated
        BatchReview --> EntityCollection : Revise feedback received
    }

    ResearchI --> CurationI : All W1-4 artifacts through >= 1 review

    state CurationI {
        [*] --> GapAnalysis : RP identifies gaps
        GapAnalysis --> DirectionAdjust : Action items defined
    }

    CurationI --> ResearchII : Gaps identified, direction set

    state ResearchII {
        [*] --> AddressGaps : Respond to curation feedback
        AddressGaps --> BuildArtifacts : Code, databases, diagrams
        BuildArtifacts --> ERDraft : Initial ER diagrams drawn
    }

    ResearchII --> Synthesis : Curation feedback addressed

    state Synthesis {
        [*] --> Integration : Cross-artifact integration
        Integration --> Capstone : Capstone draft ready
        Capstone --> GrillMe : Self-administered grill-me test
    }

    Synthesis --> Polish : Framework coherent, grill-me gaps known

    state Polish {
        [*] --> FinalCuration : Last RP review passes
        FinalCuration --> Refinement : Weak points shored up
    }

    Polish --> Close : Repository clean and complete

    state Close {
        [*] --> FinalReview : RP final review
        FinalReview --> Offboarding : Accounts reviewed
        Offboarding --> Retrospective : Next steps discussed
    }

    Close --> [*] : Program complete

    note left of Onboard : Week 1
    note left of Learn : Week 2
    note left of ResearchI : Weeks 3-4
    note left of CurationI : Weeks 4-5
    note left of ResearchII : Weeks 5-6
    note left of Synthesis : Weeks 6-7
    note left of Polish : Weeks 7-8
    note left of Close : Week 8

    note right of Onboard : Up to 3-week buffer\navailable at any phase\nfor interruptions.
```

**Cross-references:**
- [`INTERNSHIP_SPECIFICATION.md`](../../Internship/INTERNSHIP_SPECIFICATION.md) §8 — Full phase map with Gantt timeline
- [`PROSPECTIVE_INTERN_GUIDE.md`](../../Internship/PROSPECTIVE_INTERN_GUIDE.md) §"The Cadence" — Narrative walkthrough of each phase
- [`ONBOARDING_CHECKLIST.md`](../../Internship/ONBOARDING_CHECKLIST.md) — Detailed Week 1 checklist
