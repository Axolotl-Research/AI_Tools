---
title: "FAQ — Common Problems & Solutions"
audience: [interns]
last_updated: 2026-06-03
version: "1.0.0"
status: "Active"
domain: "Internship Program Management"
---

# Frequently Asked Questions

**Purpose:** Solutions for common problems you may encounter in the first weeks. Try these before escalating to WhatsApp. If the solution here does not work, or if your problem is not listed, ask in the Axolotl Interns group chat.

---

## GitHub Problems

### "Permission denied (publickey)" when I try to push

**What it means:** GitHub does not recognize your computer. You need to set up SSH keys or use a personal access token.

**Fix:**
- 🟢 [GitHub Docs: Connecting to GitHub with SSH](https://docs.github.com/en/authentication/connecting-to-github-with-ssh) — Step-by-step setup
- 🟢 [GitHub Docs: Creating a personal access token](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens) — Alternative method
- Ask Cline: "Walk me through setting up SSH keys for GitHub on my machine"

### "Failed to push some refs" or "Updates were rejected"

**What it means:** Someone else (or you, on another machine) pushed changes that you do not have locally.

**Fix:**
```bash
git pull origin main
# Resolve any conflicts, then:
git push origin main
```
- 🟢 [GitHub Docs: Resolving merge conflicts](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/addressing-merge-conflicts/resolving-a-merge-conflict-on-github)

### "fatal: not a git repository"

**What it means:** You are not inside a folder that Git is tracking.

**Fix:**
```bash
# Check if you are in the right folder
pwd
# Initialize a new repo if needed
git init
# Or clone your existing repo
git clone https://github.com/Axolotl-Research/your-repo-name.git
```

### I committed something I should not have (like a `.db` file)

**Fix:**
- 🟢 [GitHub Docs: Removing files from a repository's history](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/removing-sensitive-data-from-a-repository)
- Make sure your `.gitignore` file includes `*.db`, `*.sqlite`, and `*.sqlite3`

### My commit message is bad. How do I write a good one?

**Good commit messages:**
- Start with a verb: "Add research on lacto-fermentation organisms"
- Be specific: not "Update stuff" but "Add CSV of Swiss fermenters with Zürich producers"
- Reference relevant curation feedback: "Address Ivan's Revise on organism taxonomy"

**Resources:**
- 🟢 [Conventional Commits](https://www.conventionalcommits.org/) — A standard format (optional, but good practice)
- Ask Cline: "Write a good commit message for this change: [describe what you did]"

---

## Cline Problems

### Cline will not start / cannot connect

**Possible causes and fixes:**
1. **API key issue.** Check that your API key is configured correctly in Cline's settings.
2. **Network issue.** Cline needs internet access to reach the model provider. Check your connection.
3. **Rate limiting.** If you have been making many requests rapidly, you may be temporarily rate-limited. Wait a few minutes and try again.

If none of these work: WhatsApp the group. This is not a productive-struggle problem — it is a tool access problem.

### Cline is giving me wrong or hallucinated answers repeatedly

**What to do:**
1. Start a fresh session. Long conversations degrade.
2. Rephrase your prompt more specifically.
3. Ask Cline to cite sources, then verify them yourself.
4. Try the same question in KiloCode or Zed Agent to compare.
5. If the error is persistent and domain-critical, flag it in your artifact (`[Unverified — Cline claims X]`) and WhatsApp Ivan.

**Resources:**
- 🟢 See [`YOUNG_RESEARCHER_GUIDE.md`](YOUNG_RESEARCHER_GUIDE.md) §2 — The Verification Reflex
- 🟡 [Anthropic: Reducing Hallucinations](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/reduce-hallucinations)

### Cline is stuck in a loop — repeating the same answer

**Fix:** Start a fresh session. This is a context-window issue. The old conversation has filled the available space, and Cline cannot reason clearly. A new session gives it a clean slate.

### I do not know what to ask Cline

**Prompt starters for entity collection:**
- "List the 10 most important entities in [domain] and describe each in one paragraph."
- "What are the major academic institutions researching [domain]? For each, provide their location, focus area, and a URL."
- "I am building a CSV of [entity type]. Help me define the columns I should include."
- "What are the most important regulations governing [domain]? For each, give the official name, the governing body, and the year enacted."

**Prompt starters for relationship mapping (Weeks 5+):**
- "How does [entity A] relate to [entity B]? Describe the relationship and its significance."
- "Generate a mermaid ER diagram showing the relationships between [list 5-10 entities]."
- "What relationships am I missing in my framework? Here are my current entities: [list them]."

---

## KiloCode & Zed Problems

### I have not used KiloCode or Zed yet. Is that a problem?

**No.** Your primary tool for Summer 2026 is Cline. Adopt KiloCode and Zed Agent when:
- Cline is stuck and you want a second opinion
- You want to compare AI outputs on the same prompt
- You are building something that works better in another tool (you will discover this through experimentation)

There is no deadline for adopting additional tools. You may use only Cline for the entire program if that serves your research.

### When should I use Zed instead of Cline?

Zed is best for:
- Editing and previewing markdown files (its markdown preview is excellent)
- Making targeted edits to existing files (select text, `Ctrl+Enter`, ask the AI about it)
- Working with mermaid diagrams (Zed renders them inline)

Cline is better for:
- Multi-step research sessions with terminal access
- Building and running code
- Complex, multi-turn research conversations

---

## WhatsApp & Communication

### When should I message the group vs. just keep working?

**Message the group when:**
- You have tried three genuinely different approaches to a problem and made no progress
- You are stuck on a tool issue (cannot push, cannot connect, account not working)
- You need domain expertise to verify or disambiguate an AI claim
- You have not heard back from a curation batch review in over 4 days
- You feel frustrated AND bored/defeated (not just frustrated — that is productive struggle)

**Keep working when:**
- The AI gave you a confusing answer but you have not tried rephrasing yet
- You hit a dead end but have not tried a different AI tool or a fresh session
- You are confused but curious — the confusion is specific and you can articulate what you do not understand
- You are frustrated but also learning — each attempt gets you closer

**Rule of thumb:** Three different approaches, no progress = escalate.

### I feel like I am bothering the team with too many questions.

You are not. The WhatsApp group exists for exactly this purpose. The team would rather you ask early than struggle silently for hours. Matt ensures someone responds promptly. If you ever feel hesitant, remember: asking questions is how beginners learn, and your questions are data for the research team — they reveal the shape of the domain from the outside.

---

## Curation & Feedback

### I got a Revise decision and I disagree with it.

This is fine. Curation is a dialogue, not a decree. Do not ignore the decision — address it directly. Write your perspective in the `intern_notes` field of the curation log. Example: "I understand the concern about shallow organism taxonomy, but I believe the regulatory analysis needs the entity foundation first. Proposing we defer the taxonomy expansion to Week 6." Discuss in WhatsApp if needed.

### All my curation decisions are Revise. Am I failing?

**No.** A Revise is not a criticism — it is a map of the gap between your current understanding and expert understanding. That gap is why you are here. Early in the program, most decisions will be Revise. As your entity collection becomes more accurate, you will see Revise shift toward Merge. This shift is visible in your `CURATION_LOG.md` — it is one of the most satisfying patterns in the program.

### What if I have not received a curation review in over 4 days?

WhatsApp the group: "Hi, I submitted artifacts on [date] and have not seen a curation review yet. Just checking in!" This is not pushy — it is helping the team stay on cadence.

---

## Entity-Relationship Diagrams (Mermaid)

### I do not know how to start drawing an ER diagram.

**Step-by-step:**
1. List your 5-10 most important entities on paper (or in a markdown file).
2. Ask Cline: "Generate a mermaid ER diagram for these entities: [list them]. Show me the syntax."
3. Copy the output into a `.md` file in your repo and preview it in Zed or on GitHub.
4. Refine: add attributes to each entity, add missing relationships, ask Cline to suggest relationships you may have missed.

**Resources:**
- 🟢 [Mermaid Live Editor](https://mermaid.live/) — Experiment without committing anything
- 🟢 [Mermaid ER Diagram Guide](https://mermaid.js.org/syntax/entityRelationshipDiagram.html)
- Ask Cline: "Explain entity-relationship diagrams to a beginner. Show me a simple example."

### My ER diagram looks messy and I cannot fit everything.

That is a sign your framework is growing. Strategies:
1. Split into multiple diagrams: one for core entities, separate diagrams for sub-domains.
2. Simplify: not every entity needs to be on one diagram. Focus on the most important relationships.
3. Use Cline to reorganize: "Here is my mermaid ER diagram. It is getting too complex. Suggest a cleaner structure."

### When should I start drawing ER diagrams?

Start experimenting in Week 3-4, once you have enough entities to connect. Your first diagrams will be rough — that is expected. By Week 5-6, ER diagrams should be a regular part of your workflow. By Week 7-8, polished ER diagrams should be central to your deliverable.

---

## General

### I feel overwhelmed. There is too much to learn.

This is normal. You are learning four new tools, a new domain, and a new way of researching — all at once. Remember:
- You do not need to learn all four AI tools. Start with Cline.
- You do not need to read all the documentation. Skim the dictionary, read the Young Researcher's Guide, and return to them as needed.
- You do not need to cover everything in your domain. The deliverable is a framework, not an encyclopedia.
- Twenty hours a week is enough. Pace yourself.
- The WhatsApp group is there. Use it.

### What if I fall behind?

The program has a 3-week buffer. You cannot "fall behind" in a program designed with 37.5% slack. If life interrupts, pause. Extend. The only fixed resource is the team's availability during the summer window.

### I do not know if I am doing this right.

Share an artifact in WhatsApp and ask: "Is this the kind of thing I should be producing in Week 2?" The team would rather give you early course correction than let you drift for weeks. Early feedback is cheaper than late rework.

---

## Quick Reference: When to Escalate

| Situation | Try This First | Then Escalate |
|-----------|---------------|---------------|
| Git push fails with "Permission denied" | GitHub SSH setup guide | WhatsApp |
| Git merge conflict | GitHub merge conflict guide, ask Cline | WhatsApp |
| Cline will not connect | Check API key and network | WhatsApp immediately |
| Cline hallucinating | Fresh session, rephrase, verify | Flag in artifact; WhatsApp Ivan if critical |
| Cline looping | Fresh session | WhatsApp if fresh session does not work |
| Stuck on research question | Three different approaches | WhatsApp |
| No curation review in 4+ days | — | WhatsApp |
| Feeling overwhelmed | Re-read philosophy section of prospectus guide | WhatsApp |
| Account not working | Check password/credentials | WhatsApp immediately |
| Anything involving data loss | — | WhatsApp immediately |

---

**Still stuck?** WhatsApp the Axolotl Interns group. That is what it is for.
