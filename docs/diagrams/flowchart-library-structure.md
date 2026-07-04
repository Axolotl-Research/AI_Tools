# Library Structure

**Diagram type:** flowchart — shows the simplified reading library's five folders, their file counts, key resources, and how they map to internship domains and competency areas. Serves as the reference architecture for the library.

The library was simplified to five core folders. Each folder maps to specific research needs in the 8-week program. Use this diagram to understand which folder to browse for your current research phase. For detailed relevance descriptions per file, see [`Library/INDEX.md`](../../Internship/Library/INDEX.md).

```mermaid
flowchart TD
    subgraph Library["Reading Library — 110 files"]
        direction TB

        subgraph DomainFolders["Domain-Specific"]
            DA[Domain A<br/>Food Systems<br/>8 files]
            DB[Domain B<br/>Tokenization<br/>8 files]
        end

        subgraph CrossCutting["Cross-Cutting"]
            CST[Complexity &<br/>Systems Thinking<br/>20 files]
            RM[Research<br/>Methodology<br/>17 files]
        end

        subgraph Supplementary["Supplementary"]
            MAIA[MAIA Substack<br/>57 files<br/>Posts + Guidebook]
        end
    end

    subgraph Program["Internship Components"]
        DIR[Intern A<br/>Fermented Foods]
        DIR2[Intern B<br/>RWA Tokenization]
        COMP[Competency Areas<br/>AI_RESEARCH_LITERACY.md]
        CYCLE[Research Cycle<br/>prompt → synthesize →<br/>document → commit → curate]
    end

    DA -->|Primary source| DIR
    DB -->|Primary source| DIR2
    CST -->|ER modeling, emergence| DIR
    CST -->|ER modeling, emergence| DIR2
    RM -->|Verification, forecasting| DIR
    RM -->|Verification, forecasting| DIR2
    MAIA -->|Complexity, cognition,<br/>biology, investment| DIR
    MAIA -->|Complexity, cognition,<br/>biology, investment| DIR2

    DA -->|Domain vocabulary| COMP
    DB -->|Domain vocabulary| COMP
    CST -->|Systemic thinking| COMP
    RM -->|Research skills| COMP

    CST -->|Feedback loops,<br/>leverage points| CYCLE
    RM -->|Methodology,<br/>productive struggle| CYCLE
```

**Cross-references:**
- [`Library/INDEX.md`](../../Internship/Library/INDEX.md) — Full file listing with relevance annotations
- [`flowchart-program-architecture.md`](flowchart-program-architecture.md) — How the library fits into the overall program
- [`AI_RESEARCH_LITERACY.md`](../../Internship/AI_RESEARCH_LITERACY.md) — The 8 competency areas each folder supports
