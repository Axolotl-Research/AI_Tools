# Document Navigation Map

**Diagram type:** flowchart — a decision tree that routes new interns and research professionals to the right document based on what they need to do. Designed as a "how-to" reference to replace blind skimming with targeted reading.

Use this diagram when you are unsure which document to open. Start at the top and follow the branches matching your situation. Each terminal node links to the specific document. For the full document listing, see [`Internship/README.md`](../../Internship/README.md).

```mermaid
flowchart TD
    START([I need to...])

    START --> Q1{Am I a new intern?}

    Q1 -->|Yes, Week 1| ONBOARD[📄 ONBOARDING_CHECKLIST.md<br/>Day-by-day checklist]
    Q1 -->|Yes, before start| PROSPECT[📄 PROSPECTIVE_INTERN_GUIDE.md<br/>What to expect]
    Q1 -->|No| Q2{What is my role?}

    Q2 -->|Research Professional| Q3{What do I need?}
    Q3 -->|Program overview| SPEC[📄 INTERNSHIP_SPECIFICATION.md<br/>Full DDMVSS framework]
    Q3 -->|Curation workflow| SPEC
    Q3 -->|Artifact quality bar| EXCEL[📄 WRITING_EXCELLENCE.md<br/>Four writing tests]

    Q2 -->|Intern, past Week 1| Q4{What do I need?}

    Q4 -->|Understand a concept| LIT[📄 AI_RESEARCH_LITERACY.md<br/>8 competency areas]
    Q4 -->|Learn to prompt| CHEAT[📄 PROMPT_CHEAT_SHEET.md<br/>Phase-specific prompts]
    Q4 -->|Improve research quality| YOUNG[📄 YOUNG_RESEARCHER_GUIDE.md<br/>Verification, entity-relationship]
    Q4 -->|Understand tool landscape| SOUP[📄 AI_ALPHABET_SOUP.md<br/>MCP, ACP, A2A explained]
    Q4 -->|Find learning resources| LINKS[📄 CURATED_LINKS.md<br/>Free resources by topic]
    Q4 -->|Getting started with tools| QUICK[📄 TOOL_QUICKSTART.md<br/>GitHub, Cline, Zed, KiloCode]
    Q4 -->|I'm stuck| FAQ[📄 FAQ.md<br/>Common Week 1 problems]
    Q4 -->|Start reading| IDX[📄 Library/INDEX.md<br/>Curated reading by competency]
    Q4 -->|Improve my writing| EXCEL

    Q4 -->|Understand the spec| SPEC

    ONBOARD --> DONE([Done — follow checklist])
    PROSPECT --> DONE2([Done — then read ONBOARDING_CHECKLIST])
    SPEC --> DONE3([Done])
    LIT --> DONE4([Done — skim first, reference later])
    CHEAT --> DONE5([Done — keep it open while prompting])
    YOUNG --> DONE6([Done — re-read often])
    SOUP --> DONE7([Done])
    LINKS --> DONE8([Done])
    FAQ --> DONE9([Done — check FAQ first before WhatsApp])
    IDX --> DONE10([Done])
    EXCEL --> DONE11([Done — use for self-review])
    QUICK --> DONE12([Done])
```

**Cross-references:**
- [`Internship/README.md`](../../Internship/README.md) — Complete document listing with audience and purpose
- [`PROSPECTIVE_INTERN_GUIDE.md`](../../Internship/PROSPECTIVE_INTERN_GUIDE.md) — Start here if you are considering the internship
- [`ONBOARDING_CHECKLIST.md`](../../Internship/ONBOARDING_CHECKLIST.md) — Week 1 day-by-day walkthrough
