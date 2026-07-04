# Program Architecture

**Diagram type:** flowchart — shows how the internship program's structural components (interns, research professionals, domains, documents, and tool surfaces) fit together as a system. Serves as the reference architecture diagram for the entire program.

This diagram is the "map of the territory" — use it when you need to understand how a specific document, role, or tool relates to the larger program structure. For step-by-step navigation, see [`flowchart-document-navigation.md`](flowchart-document-navigation.md). For the 8-week timeline, see [`INTERNSHIP_SPECIFICATION.md`](../../Internship/INTERNSHIP_SPECIFICATION.md) §8.

```mermaid
flowchart TD
    subgraph People["People"]
        InternA[Intern A<br/>Domain A]
        InternB[Intern B<br/>Domain B]
        RP_Matt[Matt<br/>Program Manager]
        RP_Mike[Mike<br/>Team Navigator]
        RP_Ivan[Ivan<br/>Domain Expert]
        RP_Mario[Mario<br/>AI Methodology]
    end

    subgraph Domains["Summer 2026 Domains"]
        DA[Domain A<br/>Fermented Food Systems<br/>& Swiss Food Ecosystem]
        DB[Domain B<br/>Asset Tokenization<br/>& Cryptocurrencies]
    end

    subgraph Docs["Core Documents"]
        SPEC[INTERNSHIP_SPECIFICATION.md<br/>9-category DDMVSS framework]
        GUIDE[PROSPECTIVE_INTERN_GUIDE.md<br/>Philosophy, tools, cadence]
        YOUNG[YOUNG_RESEARCHER_GUIDE.md<br/>How to research with AI tools]
        LIT[AI_RESEARCH_LITERACY.md<br/>8 competency areas]
        EXCEL[WRITING_EXCELLENCE.md<br/>4 writing tests]
        CHEAT[PROMPT_CHEAT_SHEET.md<br/>Phase-specific prompts]
        ONBOARD[ONBOARDING_CHECKLIST.md<br/>Week 1 day-by-day]
        FAQ[FAQ.md<br/>Common problems]
    end

    subgraph Tools["Tool Surfaces"]
        GH[GitHub<br/>Persistence & curation]
        CLINE[Cline<br/>AI-assisted research]
        KILO[KiloCode<br/>AI-assisted research]
        ZED[Zed Agent<br/>AI-assisted editing]
        WA[WhatsApp<br/>Coordination & release valve]
    end

    subgraph Library["Reading Library"]
        LIB_A[Domain A<br/>Food Systems]
        LIB_B[Domain B<br/>Tokenization]
        LIB_COMPLEX[Complexity<br/>& Systems Thinking]
        LIB_METHOD[Research<br/>Methodology]
        LIB_MAIA[MAIA<br/>Substack]
    end

    InternA --> DA
    InternB --> DB
    DA --> Tools
    DB --> Tools

    RP_Matt -->|Program quality| InternA
    RP_Matt -->|Program quality| InternB
    RP_Mike -->|Communication health| InternA
    RP_Mike -->|Communication health| InternB
    RP_Ivan -->|Domain expertise| DA
    RP_Ivan -->|Domain expertise| DB
    RP_Mario -->|AI methodology| InternA
    RP_Mario -->|AI methodology| InternB

    InternA --> Docs
    InternB --> Docs
    RP_Matt --> Docs
    RP_Mike --> Docs

    Docs --> Library

    RP_Matt -->|Curation decisions| GH
    RP_Ivan -->|Domain review| GH
    RP_Mario -->|Methodology review| GH
```

**Cross-references:**
- [`INTERNSHIP_SPECIFICATION.md`](../../Internship/INTERNSHIP_SPECIFICATION.md) — Full program specification with all 11 categories
- [`Internship/README.md`](../../Internship/README.md) — Program portal with document index
- [`flowchart-document-navigation.md`](flowchart-document-navigation.md) — Which document to read and when
