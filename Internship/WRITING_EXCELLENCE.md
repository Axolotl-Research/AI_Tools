---
title: "Writing Excellence Protocol — Internship Artifacts"
audience: [interns, research-professionals]
last_updated: 2026-06-03
version: "0.3.0"
status: "Active"
domain: "Internship Program Management"
ddmvss_categories: [curation]
---

# Writing Excellence Protocol

## For Axolotl Partners Internship Research Artifacts

**Purpose:** This protocol defines what makes a research artifact excellent — not just "done," but genuinely useful to another human and consumable by an AI agent. It uses a four-dimension quality framework (Hopper, Lovelace, Schriver, Gentle) tailored to the specific artifacts you produce: markdown research files, CSV datasets, JSON exports, mermaid ER diagrams, README files, and capstone deliverables.

**Why this matters:** Your artifacts are not homework. They are the permanent record of your research. Three months after the internship ends, Ivan should be able to open your repository, read your artifacts, and understand your framework without calling you. An AI agent should be able to consume your work as ground truth and produce correct answers. The grill-me skill should find substance, not gaps. These four tests ensure that happens.

---

## 1. The Four Tests

Every artifact you submit for curation should pass at least three of these four tests. Different artifact types naturally emphasize different dimensions — a CSV will score higher on Precision (Lovelace) than Accessibility (Hopper); a README will score higher on Findability (Schriver) than Precision. That is expected. But an artifact that passes only one test is not ready for curation.

| Score | Meaning | What To Do |
|-------|---------|------------|
| **1 of 4 passes** | Not ready | Rework before submitting for curation. |
| **2 of 4 pass** | Acceptable | Submit for curation; expect Revise feedback on the two missing dimensions. |
| **3 of 4 pass** | Excellent | Submit confidently. The missing dimension is a growth target, not a flaw. |
| **4 of 4 pass** | Exceptional | Rare. This artifact could serve as an example for future interns. |

**The goal is 3 of 4.** Different artifacts emphasize different dimensions. Passing only 1 means the artifact is not ready.

---

### 1.1 Hopper Test — Accessibility

> *Can a reader with zero prior context understand this artifact by reading only what is written?*

Named for Rear Admiral Grace Hopper — author of the first computer manual (1946), inventor of the first compiler, and lifelong advocate for making machines speak human. Hopper believed that if the audience cannot understand it, the writer has failed.

**What this means for your artifacts:**

A markdown file about Swiss fermentation organisms should be comprehensible to Matt, who knows business but not microbiology. A CSV of token standards should be readable by Ivan, but also by a future intern who has never studied crypto. Your README should explain your repository to someone who was not in the WhatsApp group with you.

**Operational rules:**

| Rule | Bad Example | Good Example |
|------|-------------|--------------|
| Define terms on first use. | "Lacto-fermentation is mediated by LAB." | "Lacto-fermentation is a preservation method driven by lactic acid bacteria (LAB) — microorganisms that convert sugars into lactic acid." |
| Spell out acronyms. | "The FSVO regulates MCP under SR 817.0." | "The Swiss Federal Food Safety and Veterinary Office (FSVO) regulates fermented milk products under Swiss Regulation SR 817.0." |
| Use the reader's vocabulary. | "The substrate undergoes anaerobic glycolysis via the Embden-Meyerhof-Parnas pathway." | "The food material (substrate) is broken down without oxygen (anaerobic) through a series of chemical reactions that produce lactic acid." |
| Assume intelligence, not knowledge. | No explanation at all — assumes the reader already knows. | Explain the concept, then trust the reader to follow the implications. |
| Connect ideas explicitly. | Two paragraphs about different organisms with no transition. | "While Lactobacillus dominates dairy fermentation, a different set of organisms drives vegetable fermentation. In sauerkraut, for example..." |

**Self-check before submitting for curation:**
- [ ] Could Mario (who knows AI, not your domain) understand this artifact?
- [ ] Are all acronyms spelled out on first use?
- [ ] Are domain-specific terms defined in context or linked to your lexicon?
- [ ] Does each paragraph flow logically into the next?

---

### 1.2 Lovelace Test — Precision

> *Could a reader independently verify the claims in this artifact or reproduce your work from this description alone?*

Named for Ada Lovelace — whose 1843 Notes on the Analytical Engine described a machine that did not yet exist with such precision that her specification remains independently verifiable 180 years later. Lovelace proved that precision is not about complexity — it is about enough detail that someone else can check your work.

**What this means for your artifacts:**

If you claim that "Agroscope researchers identified three dominant Lactobacillus strains in Swiss raw milk," a reader should be able to find that Agroscope paper. If you describe an ERC-721 deployment, someone should be able to reproduce it from your instructions. If you list Swiss fermenters in a CSV, the column meanings should be unambiguous, and the data should be traceable to sources.

**Operational rules:**

| Rule | Bad Example | Good Example |
|------|-------------|--------------|
| Cite sources for factual claims. | "Swiss fermentation is dominated by small producers." | "As of 2024, over 80% of Swiss fermented food producers employ fewer than 10 people (Swiss Federal Statistical Office, 2024)." |
| Document your data schema. | A CSV with columns named `type`, `loc`, `org`. | A `schema.md` explaining: `type` = fermentation category (lacto/acetic/alcoholic), `location` = canton and municipality, `organism` = primary microbial species. |
| Make processes reproducible. | "Deploy the token, then test it." | Step-by-step instructions with exact commands, expected outputs, and troubleshooting for common errors. |
| Flag uncertainty explicitly. | Presenting an AI-generated claim as fact. | "[Cline-generated, unverified] — claimed that Gustav Gerig AG was founded in 1932. Pending confirmation from the company register." |
| Be specific about numbers. | "Many producers" or "significant growth." | "47 producers identified" or "23% increase in new fermenter licenses between 2020 and 2024." |

**Self-check before submitting for curation:**
- [ ] Are factual claims backed by sources (URL, paper citation, or official document)?
- [ ] Are AI-generated claims flagged as `[unverified]` if you could not confirm them?
- [ ] If this artifact contains data (CSV/JSON), is there a `schema.md` explaining every column?
- [ ] Could Ivan independently verify the three most important claims in this artifact?

---

### 1.3 Schriver Test — Findability

> *Can a reader find the answer to their specific question within 30 seconds of arriving at this document or repository?*

Named for Karen Schriver — whose 1997 book *Dynamics in Document Design* proved that document quality is measurable by reader outcomes, not author intent. Schriver showed that readers scan, jump, and hunt — they do not read linearly — and documents must be designed for this reality.

**What this means for your artifacts and repository:**

Your README should function as a map. Your markdown files should have scannable headings. Your ER diagrams should be visible at a glance, not buried in a folder. A research professional doing a batch review should be able to find what they need without asking you where it is.

**Operational rules:**

| Rule | Bad Example | Good Example |
|------|-------------|--------------|
| Use descriptive headings. | `## Section 1` | `## Lacto-Fermentation: Organisms and Pathways` |
| Index your artifacts. | No README, or a README that says "Welcome to my repo." | README with a table of contents linking to every major artifact, organized by phase or domain area. |
| Put diagrams where they are referenced. | "See `diagrams/erd_v3_final.md` for the entity map." | Embed the mermaid ER diagram directly in the README or the relevant markdown file, so the reader sees it in context. |
| Structure for scanning. | A wall of text with no headings, no bold, no lists. | Short paragraphs under descriptive headings, with key terms bolded and lists for scannable information. |
| Name files descriptively. | `notes1.md`, `stuff.csv`, `final_v2_real.md`. | `swiss-fermenter-directory.csv`, `lacto-fermentation-taxonomy.md`, `erc-721-deployment-guide.md`. |

**Self-check before submitting for curation:**
- [ ] Can a reader identify what this artifact is about from the filename alone?
- [ ] Can a reader find the three most important facts in this artifact within 30 seconds?
- [ ] Is your README an accurate map of your repository right now (not two weeks ago)?
- [ ] Are your ER diagrams embedded where they are discussed, not just linked?

---

### 1.4 Gentle Test — Agent-Correctness

> *If an AI agent consumed this artifact as its sole source of truth about your domain, would it behave correctly?*

Named for Anne Gentle — whose 2017 book *Docs Like Code* established that documentation shares code's lifecycle: version control, continuous integration, review, and contributor workflows. In an agent-native system, stale or imprecise documentation is not a cosmetic issue — it is a functional defect that produces incorrect agent behavior.

**What this means for your artifacts:**

When Cline reads your markdown file about Swiss food regulations and uses it to answer Ivan's question, will the answer be correct? When the grill-me skill consumes your ER diagram and interrogates you on relationships, will it find real substance? When a future AI tool indexes your repository, will it extract accurate structured knowledge or garbled noise?

**Operational rules:**

| Rule | Bad Example | Good Example |
|------|-------------|--------------|
| Write facts, not fluff. | "Swiss fermentation is a rich and fascinating tradition with deep cultural roots." | "Switzerland has three major fermented food categories by production volume: dairy (cheese, yogurt), vegetable (sauerkraut, pickles), and baked (Bürli, Ruchbrot)." |
| Structure data for machines. | A CSV with inconsistent formatting, missing headers, or mixed data types in one column. | Clean CSV with consistent types, documented headers, and a companion `schema.md`. |
| Keep artifacts synced with each other. | README references an artifact that was renamed. Two markdown files contradict each other on the same fact. | Cross-reference updates propagate. When you rename a file, update every link to it. |
| Version-control everything. | "I have the latest version on my laptop — I'll push it later." | Every meaningful change is committed and pushed. The repo is always the source of truth. |
| Use consistent terminology. | Calling the same entity "Swiss Food Safety Office" in one file and "FSVO" unexplained in another. | Use the term defined in your lexicon. Link to it. Be consistent. |

**Self-check before submitting for curation:**
- [ ] If Cline read only this artifact and answered a domain question, would the answer be correct?
- [ ] Is the terminology in this artifact consistent with your other artifacts?
- [ ] If this artifact references another file, is the link correct and the referenced file current?
- [ ] Would the grill-me skill find substance or gaps in this artifact?

---

## 2. Voice and Style Standards

Your artifacts are research, not software specifications, so these standards are lighter than a full specification protocol — but the principles translate directly.

### 2.1 Voice

| Dimension | Standard |
|-----------|----------|
| **Register** | Clear, direct, and precise. No filler, no hedging, no academic bloat. |
| **Person** | First person is fine for reflection and intern notes. Third person for factual claims. "I identified 47 Swiss fermenters" is fine. "Fermenters are concentrated in cantons Bern and Zürich" is better for factual claims. |
| **Tense** | Present tense for current-state descriptions. Past tense for historical context. "Agroscope was founded in..." / "Agroscope currently researches..." |
| **Confidence** | Assert what you have verified. Flag what you have not. "Lactobacillus is the dominant genus in dairy fermentation" (verified). "Cline claims Leuconostoc may also play a significant role" (unverified). |

### 2.2 Sentence Construction

- Keep sentences under 35 words. Split if needed.
- One idea per sentence. One claim per paragraph.
- Active voice: "Agroscope studies fermentation" not "Fermentation is studied by Agroscope."
- Define technical terms on first use.

### 2.3 Structural Discipline for Markdown Artifacts

Every research artifact should follow this pattern:

1. **What this is** — one sentence describing the artifact and its purpose
2. **Key findings** — the most important claims, up front (not buried at the bottom)
3. **Evidence** — sources, data, or reasoning supporting the claims
4. **Gaps and uncertainties** — what you do not know, what needs verification
5. **Related artifacts** — links to other files in your repo that connect to this one

### 2.4 Citation Standards

| Claim Type | Minimum Citation |
|------------|-----------------|
| Factual claim about an entity | Link to official website, paper, or authoritative source |
| AI-generated claim (unverified) | Flagged as `[unverified — Cline/KiloCode/Zed generated]` |
| Statistical claim | Link to the dataset or report the number came from |
| Regulatory or legal claim | Link to the official government source |
| Your own analysis or synthesis | No citation needed — it is your work |

---

## 3. Artifact-Type-Specific Checklists

### Markdown Research File

- [ ] **Hopper:** Could a non-expert understand this? Are terms defined?
- [ ] **Lovelace:** Are claims cited? Is uncertainty flagged?
- [ ] **Schriver:** Are headings descriptive and scannable? Can a reader find key facts in 30 seconds?
- [ ] **Gentle:** Would Cline give correct answers if it consumed only this file?

### CSV / JSON Data File

- [ ] **Hopper:** Are column names self-explanatory? Is there a `schema.md`?
- [ ] **Lovelace:** Is the data traceable to sources? Are values consistent and correctly typed?
- [ ] **Schriver:** Is the file named descriptively? Is it referenced from the README?
- [ ] **Gentle:** Could an AI agent query this data and get meaningful results?

### Mermaid ER Diagram

- [ ] **Hopper:** Are entity and relationship names clear without additional explanation?
- [ ] **Lovelace:** Are cardinalities correct? Are attributes meaningful?
- [ ] **Schriver:** Is the diagram embedded where it is discussed, not just linked?
- [ ] **Gentle:** Does the diagram capture the real structure of the domain, or is it aspirational?

### README.md

- [ ] **Hopper:** Does it explain what the repository contains and why?
- [ ] **Lovelace:** Are claims about the project accurate and current?
- [ ] **Schriver:** Does it serve as a navigable map of the entire repository?
- [ ] **Gentle:** Would an AI agent understand the repository structure from the README alone?

---

## 4. The Grill-Me Connection

The writing excellence tests and the grill-me quality bar reinforce each other. An artifact that passes 3 of 4 writing excellence tests will hold up well under grill-me interrogation. An artifact that fails 3 of 4 will crumble.

| Grill-Me Level | Which Writing Test It Probes |
|----------------|---------------------------|
| Level 1: Recall & Definition | Hopper (are terms defined?) + Lovelace (are facts precise?) |
| Level 2: Mechanism & Causation | Lovelace (are processes described precisely enough to trace?) |
| Level 3: Rationale & Tradeoffs | Lovelace (are claims substantiated?) + Gentle (does the framework support reasoning?) |
| Level 4: Edge Cases & Failure Modes | Gentle (does the artifact hold up under stress?) |
| Level 5: Synthesis & Novel Scenarios | All four — this is where gaps in any dimension surface |

**Practical use:** Before you run a grill-me self-test, run the four writing excellence tests on your key artifacts. Fix what fails at the writing level first. Then grill. The grill-me will find the remaining gaps — but it should not find gaps that basic writing discipline would have caught.

---

*The four-test framework (Hopper, Lovelace, Schriver, Gentle) is a project standard; the operational rules and artifact-specific checklists are tailored to the Axolotl Partners internship program.*
