---
title: "CURATION_LOG.md — Template & Schema"
audience: [interns, research-professionals]
last_updated: 2026-06-03
version: "1.0.0"
status: "Active"
domain: "Internship Program Management"
ddmvss_categories: [curation]
---

# CURATION_LOG.md — Template & Schema

**Purpose:** Append-only curation decision log stored at the root of each intern's GitHub repository. Every artifact reviewed by a research professional receives one row in this log.

**Location:** `<intern-repo>/CURATION_LOG.md`

---

## 1. Field Schema

| # | Field | Type | Required | Description |
|---|-------|------|----------|-------------|
| 1 | `date` | ISO 8601 date (`YYYY-MM-DD`) | ✅ | Date the curation decision was made |
| 2 | `review_batch` | string | ✅ | Batch session identifier (e.g., `Week 2 — Batch 1`, `Ad Hoc`) |
| 3 | `curator` | string | ✅ | Research professional who made the decision (Matt / Mike / Ivan / Mario) |
| 4 | `artifact` | file path + commit SHA | ✅ | Path to the reviewed artifact and the specific commit (`path/to/file.md @ abc1234`) |
| 5 | `decision` | `Merge` \| `Revise` \| `Defer` \| `Discard` | ✅ | Curation decision per DDMVSS gradient |
| 6 | `rationale` | text | ✅ | **The most important field.** What was good? What was missing? Why this decision? |
| 7 | `action_items` | checklist (markdown) | ⚠️ | Required for `Revise` and `Defer`. What the intern must do before next review. |
| 8 | `status` | `Open` \| `Resolved` \| `Superseded` | ✅ | Tracks whether action items are complete |
| 9 | `intern_notes` | text | ❌ | Optional. Intern's own reflection, questions, or context. |

---

## 2. Template

Copy this into `<intern-repo>/CURATION_LOG.md` at the start of the program:

```markdown
# CURATION LOG

> Append-only log of curation decisions. One row per reviewed artifact.
> Maintained by the intern. Reviewed by research professionals.

| Date | Batch | Curator | Artifact | Decision | Rationale | Action Items | Status | Intern Notes |
|------|-------|---------|----------|----------|-----------|-------------|--------|-------------|
| 2026-06-09 | Onboarding | Matt | `README.md @ abc1234` | Merge | Initial repo structure looks good. Domain scope clear. | — | Resolved | — |
| | | | | | | | | |
| | | | | | | | | |
```

---

## 3. Example Entries

### 3.1 Merge

| Date | Batch | Curator | Artifact | Decision | Rationale | Action Items | Status | Intern Notes |
|------|-------|---------|----------|----------|-----------|-------------|--------|-------------|
| 2026-06-16 | Week 2 — Batch 1 | Ivan | `research/lacto-fermentation-overview.md @ def4567` | Merge | Comprehensive coverage of lacto-fermentation types. Good use of Swiss-specific examples (Bürli, Molke). hLexicon terms correctly applied. | — | Resolved | Ivan suggested looking into Agroscope research papers next. |

### 3.2 Revise

| Date | Batch | Curator | Artifact | Decision | Rationale | Action Items | Status | Intern Notes |
|------|-------|---------|----------|----------|-----------|-------------|--------|-------------|
| 2026-06-18 | Week 2 — Batch 2 | Ivan | `data/swiss-fermenters.csv @ ghi7890` | Revise | Good start, but missing several key producers in Zürich and Bern regions. Column `fermentation_type` conflates lacto and acetic — split into separate columns. No `schema.md` documenting the CSV structure. | - [ ] Add Zürich producers (Gustav Gerig, Fabas)<br/>- [ ] Add Bern producers<br/>- [ ] Split `fermentation_type` into `primary_organism` and `fermentation_category`<br/>- [ ] Create `data/schema.md` | Open | Will use Cline to research missing producers. |

### 3.3 Defer

| Date | Batch | Curator | Artifact | Decision | Rationale | Action Items | Status | Intern Notes |
|------|-------|---------|----------|----------|-----------|-------------|--------|-------------|
| 2026-06-25 | Week 3 — Batch 2 | Ivan | `analysis/swiss-regulatory-framework.md @ jkl0123` | Defer | This depends on the Swiss food safety taxonomy you haven't built yet. The regulatory analysis will be stronger once the classification framework is in place. | - [ ] Complete `research/fermentation-taxonomy.md` first<br/>- [ ] Revisit this artifact in Week 5 | Open | Makes sense — I was jumping ahead. |

### 3.4 Discard

| Date | Batch | Curator | Artifact | Decision | Rationale | Action Items | Status | Intern Notes |
|------|-------|---------|----------|----------|-----------|-------------|--------|-------------|
| 2026-06-20 | Week 3 — Batch 1 | Ivan | `notes/random-thoughts.md @ mno3456` | Discard | Unstructured brainstorming notes. The useful content (Nestlé fermentation history) has already been incorporated into `research/nestle-history.md`. This file is now superseded. | — | Resolved | Agreed — consolidated and moved on. |

---

## 4. Usage Rules

1. **Append-only.** Never delete rows. The log is an audit trail. If a decision changes, add a new row referencing the old one.
2. **One row per artifact per review.** If an artifact is re-reviewed after revision, it gets a new row.
3. **`rationale` is non-negotiable.** A curation decision without rationale is not a valid decision per DDMVSS.
4. **Intern maintains the log.** Research professionals provide the decisions; the intern records them. This builds ownership and ensures accuracy.
5. **Closing entry.** At program end, add a final row summarizing the collection state. Example:

| Date | Batch | Curator | Artifact | Decision | Rationale | Action Items | Status | Intern Notes |
|------|-------|---------|----------|----------|-----------|-------------|--------|-------------|
| 2026-08-01 | Close | Matt, Ivan, Mario, Mike | `REPOSITORY (all artifacts)` | Merge | Program complete. 32 artifacts, 4 data files, 1 capstone report. Framework demonstrates solid syntax/semantics/temporal understanding. Grill-me ready. | — | Resolved | This was incredible. Walking away with real AI literacy and a fermentation framework I'll use. |
