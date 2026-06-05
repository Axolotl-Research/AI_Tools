---
title: "Prompting Cheat Sheet"
audience: [interns]
last_updated: 2026-06-03
version: "1.0.0"
status: "Active"
domain: "Internship Program Management"
---

# Prompting Cheat Sheet

**Purpose:** A quick-reference card of effective prompts for every phase of your research. Keep this open in a tab or printed beside you. The patterns will become instinct — this is your training wheels.

**How to use:** Find the phase you are in (left column), pick a prompt pattern that matches what you need, customize the `[bracketed]` parts for your domain, and paste it into Cline, KiloCode, or Zed Agent.

**Filling in the brackets:** Replace `[domain]` with your topic ("Swiss fermented food systems" or "asset tokenization"). Replace `[entity]`, `[entity A]`, `[entity B]` with specific entities from your lexicon ("lacto-fermentation," "Agroscope," "ERC-721"). Replace `[year]` with actual years. Replace `[list...]` with your actual lists. The brackets are prompts to substitute, not to keep.

---

## Phase 1: Entity Collection (Weeks 1-4)

### Starting Broad — "What exists in my domain?"

| Goal | Prompt |
|------|--------|
| **Entity inventory** | "List the 20 most important entities in [domain]. For each, give: (1) name, (2) one-sentence definition, (3) why it matters. Format as a markdown table." |
| **Institution map** | "What are the major academic institutions and companies working on [domain]? For each, provide: location, focus area, key people, and a URL to their official website." |
| **Regulatory landscape** | "What regulations govern [domain]? For each: official name, governing body, year enacted, jurisdiction, and a one-sentence summary of what it requires." |
| **Key people / organizations** | "Who are the 10 most influential organizations or people in [domain]? For each: what they do, where they are based, and why they matter." |
| **Canonical sources** | "What are the 5-10 most important books, papers, or resources that everyone in [domain] has read? For each: title, author, year, and why it is foundational." |

### Going Deep on One Entity

| Goal | Prompt |
|------|--------|
| **Entity deep-dive** | "You are a [domain] expert. Explain [entity] in depth. Cover: what it is, how it works, its history, its current state, and its future trajectory. Use specific examples. Cite sources where possible." |
| **Entity comparison** | "Compare and contrast [entity A] and [entity B]. What do they have in common? How do they differ? When would you use one vs. the other? Give concrete examples." |
| **Entity taxonomy** | "Create a taxonomy of [entity category]. Group them into types or subcategories. For each group: name, defining characteristics, and 2-3 examples." |
| **Historical timeline** | "Create a timeline of key events in the history of [entity]. For each event: date, what happened, and why it mattered. Format as a markdown table." |

### Building Your Lexicon

| Goal | Prompt |
|------|--------|
| **Glossary generation** | "Define the 20 most important terms in [domain]. For each: the term, a one-sentence definition, the Swiss German equivalent if different, and an example of the term used in a sentence." |
| **Term verification** | "I've been using the term [X] to mean [your definition]. Is this correct according to standard usage in [domain]? If not, what is the correct definition? How is the term commonly misused?" |
| **Related terms** | "What terms are closely related to [X] in [domain]? For each: define it, explain how it relates to [X], and note common confusions between them." |

---

## Phase 2: Relationship Mapping (Weeks 5-8)

### Discovering Connections

| Goal | Prompt |
|------|--------|
| **Relationship discovery** | "How does [entity A] relate to [entity B]? Describe the relationship. Is it causal, regulatory, economic, competitive, collaborative? What would break if this relationship changed?" |
| **Relationship inventory** | "Here are my entities: [list 10-20 entities]. Identify all the important relationships between them. For each relationship, name the two entities, describe the connection, and rate its importance (1-5)." |
| **Missing relationships** | "Here are the entities in my framework: [list them]. Here are the relationships I've already mapped: [list them]. What relationships am I missing? What connections would a domain expert notice that I haven't?" |
| **Relationship strength** | "For the relationship between [A] and [B], how strong is it? Is it essential (A cannot exist without B), strong (B significantly shapes A), moderate, or weak? Justify your rating." |

### Building ER Diagrams

| Goal | Prompt |
|------|--------|
| **First ER diagram** | "Generate a mermaid entity-relationship diagram for these entities: [list 5-10 entities]. Include attributes for each entity (at least 3 per entity) and relationships between them. Show me the mermaid syntax I can copy into a .md file." |
| **ER diagram refinement** | "Here is my mermaid ER diagram: [paste it]. Review it for: (1) missing entities, (2) missing relationships, (3) incorrect relationship cardinalities, (4) missing attributes. Suggest improvements." |
| **ER diagram from CSV** | "I have a CSV of [entities] with these columns: [list columns]. Generate a mermaid ER diagram that represents this data. If there are implicit relationships, make them explicit." |
| **Multi-diagram split** | "My ER diagram is getting too complex. Split it into 2-3 focused diagrams: one for core entities, one for [subdomain A], one for [subdomain B]. Keep cross-references between diagrams." |

### Temporal Analysis

| Goal | Prompt |
|------|--------|
| **Change over time** | "How has [entity or relationship] changed over the last [5/10/20] years? What were the key inflection points? What drove the changes? What is likely to change in the next 5 years?" |
| **AI's role in change** | "How is AI currently affecting [domain]? What specific tasks, processes, or decisions is AI automating or augmenting? What might AI change in the next 5 years that seems impossible today?" |
| **Before/after comparison** | "Describe [domain] as it was in [year], then as it is today, then as you predict it will be in [future year]. For each time period: key entities, key relationships, dominant technologies, regulatory environment." |

---

## Phase 3: Synthesis & Self-Curation (Weeks 6-8)

### Testing Your Own Work

| Goal | Prompt |
|------|--------|
| **Framework review** | "Read my framework document: [paste it]. Identify: (a) what is strongest — the parts that would survive expert questioning, (b) what is weakest — the parts that would crumble, (c) what is missing entirely — the gaps a domain expert would notice immediately." |
| **Grill-me self-test** | "Use the grill-me methodology to interrogate my domain framework: [paste framework]. Start at Level 1 (Recall & Definition) and escalate to Level 5 (Synthesis & Novel Scenarios). For each question I cannot answer well, flag it." |
| **Cross-artifact coherence** | "Read these three artifacts from my repository: [paste paths or content]. Do they contradict each other anywhere? Are there inconsistencies in terminology, claims, or framing? If so, identify them and suggest resolution." |
| **Deliverable structure** | "I need to turn my research into a final deliverable. My artifacts cover: [list topics]. Suggest a structure: what should the main sections be? What should go in the README? Where should the ER diagrams live? What format (report, website, program) best fits my content?" |

### Preparing for Grill-Me

| Goal | Prompt |
|------|--------|
| **Grill-me at Level 1** | "Ask me 5 recall and definition questions about [domain]. For each: ask the question, wait for my answer, then evaluate it. If I'm wrong, tell me and ask me to try again." |
| **Grill-me at Level 3** | "Ask me 5 rationale and tradeoff questions about [domain]. Probe why things are designed the way they are. When I give an answer, challenge it: 'Why not the alternative?' or 'What would break if we did the opposite?'" |
| **Grill-me at Level 5** | "Present me with a novel scenario in [domain] — something that doesn't exist yet but could. Ask me to extend my framework to accommodate it. Push back on my answers. Find the edge of my understanding." |
| **Full grill-me simulation** | "You are a demanding domain expert conducting an oral examination on [domain]. Start at Level 1 and escalate through Level 5. Be relentless. When I hand-wave, demand specifics. When I'm partially right, push on what's missing. Track my performance." |

**Note on grill-me:** The grill-me skill (created by Matt Pocock, used in KiloCode's Architect Agent) is an actual agent skill you can find and load. Discovering how to use it is part of your learning. The prompts above are a fallback if you have not yet loaded the skill — but loading the real skill will give you a more authentic grill-me experience.

---

## Core Prompting Patterns (Use in Any Phase)

### The Five Essential Patterns

| Pattern | Structure | Example |
|---------|-----------|----------|
| **Role + Task + Format** | "You are a [role]. [Task]. [Format constraint]." | "You are a Swiss food scientist. Explain lacto-fermentation in 3 bullet points, with examples from Swiss cuisine." |
| **Chain of Thought** | "Walk me through [process] step by step. At each step, explain what could go wrong." | "Walk me through deploying an ERC-20 token on Ethereum Sepolia testnet. At each step, explain what could go wrong." |
| **Verify and Correct** | "You said [claim]. That is [wrong/incomplete] because [reason]. Acknowledge the correction and revise." | "You said Lactobacillus is the only bacteria in kimchi. That's wrong — Leuconostoc is also present. Acknowledge and revise." |
| **Source Anchoring** | "[Task]. For each claim, provide a URL to an authoritative source." | "List 5 Swiss food research institutions. For each, provide a URL to their official website." |
| **Constraint Framing** | "[Task]. Constraints: [list]." | "Summarize ERC-721 in under 200 words. Focus only on the ownership model, not implementation. Use plain English." |

### When Cline Is Wrong or Stuck

| Situation | Prompt |
|-----------|--------|
| **Cline is hallucinating** | "You just said [claim]. I cannot verify this. Where did this information come from? If you are unsure, say 'I am not certain' rather than guessing." |
| **Cline is looping** | Start a fresh session. Do not continue the same conversation. |
| **Cline is too vague** | "Be more specific. Give me names, dates, numbers, and sources. If you are generalizing, tell me what you are generalizing from." |
| **Cline is too confident** | "For each claim in your last response, rate your confidence from 1-5 and explain why. If your confidence is below 4, suggest how I could verify the claim." |
| **Cline misunderstood** | "You misunderstood my question. Let me rephrase: [clearer version]. If anything is still ambiguous, ask me to clarify before answering." |

---

## Format & Structure Prompts

| Goal | Prompt |
|------|--------|
| **Markdown table** | "Format your response as a markdown table with columns: [list columns]." |
| **Mermaid diagram** | "Represent this as a mermaid [flowchart/erDiagram/sequenceDiagram/gantt]. Show me the syntax." |
| **Bullet hierarchy** | "Organize your response as nested bullets. Top level: [categories]. Second level: [details]. Third level: [examples]." |
| **CSV-ready** | "Format this data as CSV with these columns: [list]. Include a header row." |
| **Executive summary** | "Summarize your response in 3 sentences. Then provide the full detail below." |
| **Pros / cons** | "For [topic], list pros and cons. For each: one sentence and a concrete example." |
| **Timeline** | "Create a timeline of [topic] from [start year] to [end year]. For each entry: date, event, significance. Format as a markdown table." |

---

## Verification Prompts

| Goal | Prompt |
|------|--------|
| **Source check** | "For every factual claim in your response, provide a URL where I can verify it. If you cannot provide a URL, flag the claim as [unverifiable]." |
| **Second opinion** | After getting an answer from Cline, paste the same prompt into KiloCode or Zed Agent. Compare outputs. Note disagreements. |
| **Recency check** | "Is this information current as of 2026? What has changed since your training data cutoff? What should I verify independently?" |
| **Bias check** | "What perspective or assumptions are embedded in your response? What would someone who disagrees with this framing say?" |

---

## Quick Reference Card

### If you want to... → Use this pattern

| You want to... | Prompt pattern |
|----------------|---------------|
| Explore a new topic | "List the 20 most important entities in [domain]..." |
| Go deep on one thing | "You are a [domain] expert. Explain [entity] in depth..." |
| Compare two things | "Compare and contrast [A] and [B]..." |
| Find connections | "How does [A] relate to [B]? What would break if this relationship changed?" |
| Draw a diagram | "Generate a mermaid erDiagram for these entities: [list]..." |
| Test your knowledge | "Use the grill-me methodology to interrogate my framework..." |
| Verify a claim | "For every factual claim, provide a URL. Flag unverifiable claims." |
| Fix a hallucination | "You said [X]. I cannot verify this. Where did this come from?" |
| Get structure | "Format as a markdown table with columns: [list]..." |
| Build your lexicon | "Define the 20 most important terms in [domain]..." |

---

### The Three Rules of Prompting

1. **Your first prompt is rarely your best.** Iterate. Rephrase. Push back. The second or third version will be sharper.
2. **Specific beats vague every time.** "Tell me about Swiss food" → garbage. "List 10 Swiss fermented food producers, their location, founding year, and flagship product" → gold.
3. **The AI does not know what it does not know.** It will answer questions it has no business answering. Verify everything that matters.

---

**Print this. Keep it open. Use it until the patterns are instinct.**
