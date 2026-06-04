---
title: "Onboarding Checklist — Week 1 Day-by-Day"
audience: [interns]
last_updated: 2026-06-03
version: "1.0.0"
status: "Active"
domain: "Internship Program Management"
---

# Onboarding Checklist — Week 1

**Purpose:** A step-by-step checklist for your first week. Complete every item before moving on. If you get stuck on any step for more than 30 minutes, post in the WhatsApp group — that is what it is for.

**Exit criteria for Week 1** (from the specification):
> GitHub push successful; first Cline research session completed; WhatsApp introduction posted; CURATION_LOG.md initialized; domain hLexicon draft started.

**Key terms:**

| Term | Definition |
|------|------------|
| **Artifact** | Any markdown doc, code file, CSV, JSON, PDF, or agent skill you produce and store in your GitHub repository. |
| **hLexicon** | Your domain dictionary — the collection of terms with specific meaning in your domain that you build throughout the program. |
| **Curation** | The process where a research professional reviews your artifacts and records a decision: Merge, Revise, Defer, or Discard. |
| **CURATION_LOG.md** | An append-only markdown table in your repo root where every curation decision is recorded. |
| **Grill-me** | A Socratic examination skill that tests understanding through five levels: Recall, Mechanism, Rationale, Edge Cases, and Synthesis. |

---

## Day 1: Accounts & Access

- [ ] **GitHub account provisioned** — Verify you can sign in to github.com and see the Axolotl-Research organization
- [ ] **Cline installed and working** — Open Cline in your editor, type "Hello, I'm starting the Axolotl internship," confirm it responds
- [ ] **KiloCode accessible** — Verify your kilo.ai account works
- [ ] **Zed Agent accessible** — Open Zed, confirm the AI agent responds to a prompt
- [ ] **WhatsApp group joined** — Confirm you can see and post in the Axolotl Interns group
- [ ] **All five tool surfaces confirmed** — GitHub, Cline, KiloCode, Zed Agent, WhatsApp ✅

If any account is not working, escalate immediately in the WhatsApp group or contact Matt directly.

---

## Day 1-2: Repository & First Push

- [ ] **Create your repository** in the Axolotl-Research organization
  - Name it clearly (e.g., `fermented-food-systems-2026` or `asset-tokenization-2026`)
  - Initialize with a README
- [ ] **Clone your repository** to your local machine
  ```
  git clone https://github.com/Axolotl-Research/your-repo-name.git
  cd your-repo-name
  ```
- [ ] **Initialize CURATION_LOG.md** — Copy the template from [`CURATION_LOG_TEMPLATE.md`](CURATION_LOG_TEMPLATE.md) into your repo root
- [ ] **Write your first README.md** — Describe your domain and what you hope to learn
- [ ] **Stage, commit, and push**
  ```
  git add README.md CURATION_LOG.md
  git commit -m "Initial repo setup: README and curation log"
  git push origin main
  ```
- [ ] **Verify on GitHub.com** — Open your repo in the browser and confirm the commit is there

---

## Day 1-2: Orientation Reading

- [ ] **Read** [`PROSPECTIVE_INTERN_GUIDE.md`](PROSPECTIVE_INTERN_GUIDE.md) — The big picture: philosophy, tools, framework, 8-week cadence
- [ ] **Skim** [`AI_RESEARCH_LITERACY.md`](AI_RESEARCH_LITERACY.md) — Do not try to memorize. Notice what you recognize and what you don't. Return to it as concepts surface.
- [ ] **Read** [`YOUNG_RESEARCHER_GUIDE.md`](YOUNG_RESEARCHER_GUIDE.md) — How to research with probabilistic tools, how to verify, how to handle disagreement
- [ ] **Skim** [`FAQ.md`](FAQ.md) — Know it exists. Come back when you hit a problem.
- [ ] **Skim** [`READING_ROADMAP.md`](READING_ROADMAP.md) — Know what to read and when throughout the program
- [ ] **Read the MA Guidebook** — [`Library/MAIA-Substack/MA_Guidebook_July23.md`](Library/MAIA-Substack/MA_Guidebook_July23.md) — How the team thinks
- [ ] **Read the teaching-learning-and-ai post** — [`Library/MAIA-Substack/posts/137992097.teaching-learning-and-ai.html`](Library/MAIA-Substack/posts/137992097.teaching-learning-and-ai.html)

---

## Day 2-3: First Research Session

**Choose your starting path:**

- [ ] **Path A — Start with GitHub:** Create a markdown file describing your domain, push it. ✅ You have made your first artifact.
- [ ] **Path B — Start with Cline:** Prompt: "I'm researching [your domain]. Help me identify the 10 most important entities in this field." Save the conversation as a markdown file. ✅ You have made your first artifact.
- [ ] **Do the other path** — Whichever you started with, do the other one next.

- [ ] **Commit and push your first artifact**
  ```
  git add research/my-first-entity-collection.md
  git commit -m "First entity collection: top 10 entities in [domain]"
  git push origin main
  ```

---

## Day 3-4: Domain Lexicon & Curation

- [ ] **Start your domain hLexicon** — Create a file (e.g., `LEXICON.md`) with the key terms in your domain. An hLexicon is your personal domain dictionary: the terms that have specific meaning in your domain, each with a 1-2 sentence definition in your own words.
  - Include the source (AI tool, book, web resource) where you encountered each term
  - Target at least 10 terms for your first draft
- [ ] **Review your first artifact critically** — Does it hold up? Are there entities that feel thin? Entities you can't define precisely?
- [ ] **Check CURATED_LINKS.md** for your domain's section (§10) — bookmark the most relevant links
- [ ] **Explore the Library** for your domain:
  - Domain A: [`Library/Domain-A-Food-Systems/`](Library/Domain-A-Food-Systems/)
  - Domain B: [`Library/Domain-B-Tokenization/`](Library/Domain-B-Tokenization/)
- [ ] **Verify your CURATION_LOG.md** has the initial entry from Matt

---

## Day 4-5: Second Research Session & Communication

- [ ] **Conduct a second research session** — Use a different AI tool than your first session (if you used Cline, try KiloCode or Zed Agent)
- [ ] **Compare outputs** — Where do the tools agree? Where do they disagree? Write a brief note about this in your artifact.
- [ ] **Commit and push your second artifact**
- [ ] **Post a WhatsApp check-in** in the Axolotl Interns group. This is part of the program cadence — weekly check-ins keep the team connected. Include:
  - What you accomplished this week
  - What you are working on next
  - Any questions or blockers

---

## End-of-Week-1 Self-Check

Verify every exit criterion from the specification:

- [ ] **GitHub push successful** — You have at least one commit pushed to your repo
- [ ] **First Cline research session completed** — You used Cline to research your domain
- [ ] **WhatsApp introduction posted** — The group knows who you are
- [ ] **CURATION_LOG.md initialized** — Template copied and first entry logged
- [ ] **Domain hLexicon draft started** — You have a file with at least 10 key terms defined

### If You Completed All Five

You are on track. Move into Week 2 (Learn phase) — start broader research, produce your first three artifacts, and record your first curation log entry.

### If You're Stuck on Any Item

1. Check [`FAQ.md`](FAQ.md) for the specific problem
2. Try a different AI tool — if Cline is stuck, try KiloCode
3. Post in the WhatsApp group — that is the release valve
4. Remember: **struggle is productive.** You are expected to get stuck. What matters is that you unstick yourself or ask for help before frustration sets in.

---

*This checklist implements the Week 1 exit criteria defined in [`INTERNSHIP_SPECIFICATION.md`](INTERNSHIP_SPECIFICATION.md) §8.2.*