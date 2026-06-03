---
title: "The Young Researcher's Guide to AI Tools"
audience: [interns]
last_updated: 2026-06-03
version: "1.0.0"
status: "Active"
domain: "Internship Program Management"
---

# The Young Researcher's Guide to AI Tools

**Purpose:** A practical guide to doing real research when your primary tools are probabilistic, occasionally wrong, constantly evolving — and incredibly powerful when used well. This is not about which buttons to press. It is about how to think.

---

## 1. The Situation You Are In

You are a beginner researcher working with beginner tools. This is not a disadvantage — it is the entire point of the internship. But it creates a specific set of challenges that no textbook on research methods prepared you for.

Your AI tools are, in mid-2026, astoundingly capable and deeply unreliable in the same breath. They can summarize a hundred papers in seconds but will invent citations for papers that do not exist. They can explain the mechanics of ERC-721 token standards with precision but will confidently describe a deprecated version as if it is current. They can help you build a CSV database of Swiss fermenters but will populate it with companies that went out of business in 2019.

Your job is not to fix these tools. It is to learn how to *work with them anyway* — to develop the judgment, the verification habits, and the intellectual self-awareness that let you extract genuine research value from systems that are, by their nature, unreliable partners.

This guide is about that judgment.

---

## 2. The Verification Reflex

### The Single Most Important Habit

Every time an AI tool makes a factual claim, your brain should fire a signal: *verify this*. Not because the claim is likely false — many AI claims are accurate. But because you cannot tell which claims are accurate and which are hallucinated without checking, and the AI will not tell you the difference. It presents everything with the same smooth confidence.

Build this reflex early. The first week, consciously pause after every AI response that contains a factual claim — a name, a date, a regulation, a chemical pathway, a token standard, an institution — and ask:

1. *Can I find an authoritative source that confirms this?*
2. *Does this claim make sense given what I already know?*
3. *Would Ivan or Mario immediately spot an error here?*

By Week 3, this will be automatic. By Week 8, it will be instinct. This reflex is the difference between someone who *uses* AI and someone who is *AI-literate*.

### How to Verify in Practice

| Claim Type | Verification Strategy |
|------------|----------------------|
| **Academic paper exists** | Search Google Scholar, PubMed, or the journal directly. Do not trust the AI's citation — find the actual paper. |
| **Company or institution** | Go to the official website. Check the "About" page. Verify it is still operating. |
| **Regulation or law** | Find the government source. Swiss law is at fedlex.admin.ch. EU regulations at eur-lex.europa.eu. |
| **Technical specification** | Check the official documentation or specification (e.g., ethereum.org for ERC standards, the MCP spec at modelcontextprotocol.io). |
| **Historical claim** | Find at least two independent sources. AI is particularly bad at historical specificity. |
| **Statistical claim** | Find the original dataset or report. AI often invents plausible-sounding numbers. |

### When You Cannot Verify

Sometimes you will encounter a claim you cannot verify — the source is paywalled, in a language you do not read, or simply unfindable. In these cases:

1. **Flag it in your artifact.** Add a comment: `[Unverified — Cline claims X, but I could not locate the primary source.]`
2. **Ask the research team.** WhatsApp the group: "Cline says Swiss regulation SR 817.022.1 covers fermentation safety, but I cannot find it. Can anyone confirm?"
3. **Do not include unverified claims in your deliverable without flagging them.** The grill-me will find them.

---

## 3. Structuring a Research Session

### Before You Start

1. **Define the question.** Not "tell me about Swiss fermentation" but "what are the three dominant fermentation methods used by Swiss commercial producers, and how do they differ in microbial profile and regulatory classification?"
2. **Open a fresh session.** Do not carry yesterday's context into today's research. The context window is finite, and old conversation degrades new answers.
3. **Commit your current work.** That way you can always revert if the AI makes changes you do not want.

### During the Session

1. **Start broad, then narrow.** First prompt: overview. Second prompt: drill into the most interesting thread. Third prompt: challenge the AI's own claims.
2. **Write as you go.** Do not wait until the session is over to document. Draft your artifact alongside the research. The AI can help you structure and format.
3. **Save useful prompts.** You will find yourself reusing certain prompt patterns. Keep a `prompts.md` file in your repo.
4. **Note what the AI gets wrong.** These errors are data — they tell you where the boundaries of the model's knowledge lie, which is itself useful domain information.

### After the Session

1. **Commit your artifact.** Even if it is rough. A rough artifact on GitHub is better than a polished artifact in your head.
2. **Write a one-sentence reflection.** What did you learn? What surprised you? What do you need to verify? This goes in your artifact's header or in your intern notes.
3. **Check the curation log.** Is there a batch review coming? Make sure your new artifacts are ready.

---

## 4. When Two AI Tools Disagree

This will happen. Cline will tell you one thing. KiloCode will tell you another. Zed Agent will suggest a third approach entirely. This is not a malfunction — it is the most educational moment in your research week.

### Why Disagreement Happens

- **Different underlying models.** Cline, KiloCode, and Zed may use different LLMs with different training data, different knowledge cutoffs, and different behavioral tendencies.
- **Probabilistic sampling.** Even the same model, given the same prompt twice, can produce different outputs because it samples from a probability distribution, not a database.
- **Different prompt interpretations.** Slight differences in how each tool interprets your prompt lead to different research paths.
- **Genuine domain ambiguity.** Some questions — "what is the most important trend in Swiss fermentation?" — have no single correct answer. The tools are reflecting real ambiguity, not error.

### What to Do

1. **Do not panic.** Disagreement is data.
2. **Identify the nature of the disagreement.** Is it factual (one says X, the other says Y about a verifiable fact) or interpretive (different frameworks for understanding the same phenomenon)?
3. **For factual disagreements: verify.** Find the ground truth. Which tool was right? Which was wrong? Record the result — this builds your mental model of each tool's reliability for different kinds of questions.
4. **For interpretive disagreements: synthesize.** Both perspectives may be valid. Your framework can accommodate multiple interpretations. In fact, frameworks that acknowledge genuine ambiguity are stronger than frameworks that pretend everything is settled.
5. **Document the disagreement in your artifact.** "Cline argues X. KiloCode argues Y. The tension appears to stem from Z. My synthesis is..." This is exactly the kind of critical thinking that impresses in a grill-me.

---

## 5. Productive Struggle vs. Unproductive Frustration

One of the hardest skills to develop is knowing when to push through and when to reach out.

### Signs of Productive Struggle

- You feel confused, but the confusion is *specific* — you can articulate what you do not understand
- Each attempt gets you slightly closer, even if you are not there yet
- You are learning things you did not expect, even if they are not what you were looking for
- The AI's errors are teaching you something about the domain or about the tool
- You feel frustrated but also curious

**What to do:** Keep going. Rephrase your prompts. Try a different AI tool. Take a break and come back. The struggle is writing skills into your neurons.

### Signs of Unproductive Frustration

- The confusion is *global* — you cannot even articulate what you do not know
- You have tried the same thing five times with no progress
- The AI is looping — giving you the same wrong answer in different words
- You feel frustrated and also *bored* or *defeated*
- You are starting to resent the tool, the domain, or the internship

**What to do:** WhatsApp the group. Say "I am stuck on X. I have tried Y and Z. Nothing is working. Help." Someone will respond promptly. This is not failure — it is using the release valve as designed.

### A Rule of Thumb

If you have tried three genuinely different approaches to the same problem and made no progress, escalate. Three is enough to know you are not just being impatient.

---

## 6. The AI Confidence Trap

AI tools almost never express uncertainty. They do not say "I think this might be the case, but I am not sure" or "this is outside my training data, so take this with caution" or "I am guessing." They state everything with equal confidence — the true, the false, and the hallucinated.

This creates a cognitive trap. Human brains are wired to trust confident speakers. When an AI tool tells you, with perfect prose and apparent authority, that the Swiss Federal Office of Food Safety issued Regulation 817.022.1 in 2018, your brain wants to believe it. The sentence structure is correct. The tone is authoritative. The details are specific. It *feels* true.

But the AI has no mechanism for distinguishing between a memory of a real regulation and a statistically plausible fabrication. To the model, both are just token sequences with high probability given the prompt. The confidence is a property of the prose style, not of the factual accuracy.

### How to Guard Against This

1. **Treat every AI claim as a hypothesis, not a fact.** "Cline hypothesizes that..." is a better mental frame than "Cline told me that..."
2. **Notice when the AI is *too* smooth.** Real research is messy. If an AI answer feels suspiciously clean and complete, it probably skipped the messy parts — or invented them.
3. **Ask the AI to express uncertainty.** "For each claim in your response, rate your confidence from 1-5 and explain why." Some models handle this better than others, but the exercise itself is useful — it forces you to think about which claims are bedrock and which are speculation.
4. **Remember: the AI does not know what it does not know.** It has no metacognitive awareness of the boundaries of its training. It will answer questions it has no business answering with the same confidence as questions squarely in its wheelhouse.

---

## 7. Building Domain Vocabulary

A domain is inaccessible until you have its vocabulary. You cannot research Swiss fermentation if you do not know what *lacto-fermentation* means, what *Agroscope* is, or how *Bürli* differs from *Ruchbrot*. You cannot research tokenization if you do not know what *ERC-721* is, what *custody* means in a blockchain context, or how *DeFi* differs from *CeFi*.

### How to Build Vocabulary with AI

1. **Start with a glossary prompt.** "Define the 20 most important terms in Swiss fermented food production. For each, give a one-sentence definition and the Swiss German term if different from standard German."
2. **Maintain a living `GLOSSARY.md` in your repo.** Every time you encounter a new term, add it. This becomes your hLexicon — the vocabulary that grounds your framework.
3. **Ask the AI to use terms correctly, then verify.** "Write a paragraph about lacto-fermentation that correctly uses the terms *starter culture*, *substrate*, *brine*, and *anaerobic*. Then define each term."
4. **Notice when the AI misuses a term.** This is valuable domain data — it tells you which concepts the model genuinely understands and which it is faking.

### The Vocabulary Threshold

There is a point, usually around 50-100 domain terms, where something clicks. You stop translating in your head. You start thinking *in* the domain's language. The AI's outputs become easier to evaluate because you can hear when it uses a term wrong. This threshold usually arrives around Week 3-4. When it does, your research speed and depth will jump noticeably.

---

## 8. The Curation Cycle as a Learning Accelerant

Twice a week, a research professional reviews your artifacts and makes a decision: Merge, Revise, Defer, or Discard. This is not grading — it is the fastest learning mechanism in the program.

### How to Get the Most from Curation

1. **Read the rationale carefully.** The decision (Merge/Revise/Defer/Discard) is less important than the *why*. What did the expert see that you missed? What assumption did you make that does not hold?
2. **Do not get defensive.** A Revise is not a criticism of you — it is a map of the gap between your current understanding and expert understanding. That gap is why you are here. Closing it is the work.
3. **Address action items promptly.** If Ivan says "split the fermentation_type column into primary_organism and fermentation_category," do it before the next batch review. Do not let action items accumulate.
4. **Record everything in the curation log.** The `CURATION_LOG.md` is not a chore — it is the story of your intellectual development. Future you will read it and see exactly how your thinking evolved.
5. **Notice patterns in the feedback.** If three Revise decisions all point to the same weakness (e.g., "your syntax is detailed but your semantics are shallow"), that is a signal about where to focus your next research cycles.

### When You Disagree with a Curation Decision

It happens. You might think a Defer decision is premature, or that a Revise asks for changes that would take your framework in the wrong direction. In these cases:

1. **Do not ignore the decision.** Address it directly.
2. **Write your perspective in the `intern_notes` field of the curation log.** "I understand the concern about shallow semantics, but I believe the regulatory analysis needs the syntax foundation first. Proposing we defer the semantic expansion to Week 6 instead."
3. **Discuss in WhatsApp if needed.** Curation is a dialogue, not a decree.

---

## 9. Managing the Information Flood

AI tools can generate more research material in an hour than you can meaningfully process in a week. The bottleneck is not production — it is understanding. Your job is not to maximize artifact count. It is to maximize depth on the artifacts you commit to.

### Strategies

1. **One artifact per research session.** Resist the urge to produce three markdown files in one sitting. One well-verified, well-structured artifact is worth ten rough drafts.
2. **Depth over breadth.** A 500-word artifact that gets five things right is better than a 5,000-word artifact that gets fifty things half-right. The grill-me will find the half-right parts.
3. **Before starting a new artifact, ask: does this fill a gap identified in curation?** If not, consider whether it is the best use of your 20 hours this week.
4. **Use the AI to summarize your own work.** "Read my last five artifacts and identify: (a) what is strongest, (b) what is weakest, (c) what is missing entirely." This is a powerful self-curation exercise.

---

## 10. What to Do When the AI Tool Itself Changes

Cline, KiloCode, and Zed Agent are young products. They will update during your internship. A feature you relied on in Week 2 may work differently in Week 6. A model upgrade may make the tool suddenly better at some things and worse at others.

This is not a distraction from your research — it is part of your AI literacy education. The tools you will use in your career five years from now will also change, also break, also surprise you. Learning to adapt to tool evolution is itself a durable skill.

### What to Do

1. **Notice the change.** If Cline suddenly starts giving different kinds of answers, do not assume you got worse at prompting. The tool may have changed.
2. **Test the change.** Give the tool a prompt you have used before and compare the output. This tells you what shifted.
3. **Adapt your prompting.** A model upgrade may require different prompting strategies. Experiment.
4. **Document what you learn.** A `TOOL_OBSERVATIONS.md` file in your repo — noting when tools changed and how you adapted — is a genuinely interesting artifact for the research team.

---

## 11. The Beginner's Perspective Is Your Superpower

You are not an expert in fermented food. You are not an expert in tokenization. This feels like a weakness. It is not.

Experts have blind spots. They have internalized assumptions they no longer notice. They have stopped asking certain questions because "everyone knows" the answer. You do not have these blind spots yet. You see the domain with fresh eyes, and when you ask "why is this done this way?", you sometimes surface assumptions that deserve to be challenged.

The Axolotl research team is not just mentoring you — they are learning from you. Your beginner's questions, your naive observations, your confusion about things "everyone knows" — these are data. They reveal the shape of the domain from the outside, which is a perspective experts cannot access directly.

So when you feel lost, when you feel like you do not know enough, when you hesitate to ask a question because it seems obvious — ask it anyway. The question that feels too basic to you may be exactly the question that makes Ivan stop and think.

---

## 12. A Final Note on Pace

Twenty hours a week for eight weeks is 160 hours. That is enough time to go deep on one domain — and not enough time to go deep on everything. You will not learn every AI tool. You will not read every paper. You will not cover every subtopic. You will leave gaps.

This is fine. The deliverable is not "everything about fermented food" or "everything about tokenization." The deliverable is a framework — a structured way of seeing the domain that demonstrates genuine understanding of syntax, semantics, and temporal change. Frameworks have boundaries. They acknowledge what they do not cover. A framework that knows its limits is stronger than one that pretends to be comprehensive.

When you feel overwhelmed — and you will — remember: your job is not to know everything. Your job is to build a way of thinking about the domain that can survive expert questioning. That is a different task, and 160 hours is enough time to do it well.

---

**Now: open Cline, commit your first artifact, and get started.**
