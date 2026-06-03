---
title: "AI & Research Literacy — Key Terms, Principles, and Resources"
audience: [interns]
last_updated: 2026-06-03
version: "1.0.0"
status: "Active"
domain: "Internship Program Management"
---

# AI & Research Literacy Dictionary

**Purpose:** A reference for the seven AI literacy competency areas. Each entry includes a definition, why it matters to your internship, and links for deeper learning. Return to this throughout the program — some concepts will only click after you have used the tools for a few weeks.

---

## 1. Git & GitHub Basics

### Version Control
**Definition:** A system that records changes to files over time, allowing you to recall specific versions, collaborate without conflict, and revert mistakes.

**Why it matters:** Your entire internship artifact collection lives in Git. Every commit is a checkpoint. If you break something, you can always go back. If the research team wants to see how your thinking evolved, the commit history tells the story.

**Key sub-concepts:** repository, commit, branch, merge, push, pull, pull request, `.gitignore`, diff, merge conflict, rebase.

**Resources:**
- [GitHub Skills](https://skills.github.com/) — Free interactive courses from GitHub
- [Oh My Git!](https://ohmygit.org/) — A visual game that teaches Git internals
- [Atlassian Git Tutorials](https://www.atlassian.com/git/tutorials) — Comprehensive written guides
- [Git Book](https://git-scm.com/book/en/v2) — The definitive reference (free online)

### Distributed Version Control
**Definition:** Every copy of a Git repository is a full backup. There is no central server that can fail and lose everything. GitHub is a convenience, not a necessity.

**Why it matters:** Your work is never trapped on one machine. Push to GitHub and you can work from anywhere. GitHub goes down? Your local copy still has everything.

---

## 2. LLM Prompting

### Prompt Engineering
**Definition:** The practice of designing inputs to large language models to produce desired outputs. Includes role assignment, constraint specification, format demands, chain-of-thought prompting, and few-shot examples.

**Why it matters:** The quality of your research output is directly proportional to the quality of your prompts. A vague prompt produces vague research. A well-structured prompt produces structured, verifiable, actionable research. This is the single most important hands-on skill you will develop.

**Key patterns:** role + task + format, chain-of-thought, verify-and-correct, source anchoring, constraint framing, few-shot learning, iterative refinement.

**Resources:**
- [Anthropic Prompt Engineering Guide](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/overview) — Excellent, tool-agnostic principles
- [OpenAI Prompt Engineering Guide](https://platform.openai.com/docs/guides/prompt-engineering) — Complementary perspective
- [Prompt Engineering Guide (DAIR.AI)](https://www.promptingguide.ai/) — Comprehensive community resource

### Hallucination
**Definition:** When an LLM generates content that is factually incorrect, fabricated, or nonsensical, but presents it with confidence and plausible structure.

**Why it matters:** Every AI tool you use this summer will hallucinate. Cline will invent Swiss food regulations. KiloCode will cite papers that do not exist. Zed Agent will explain a token standard that was deprecated years ago. **Hallucination is not a bug — it is a fundamental property of probabilistic language models.** Your job is not to avoid it (you cannot) but to develop the reflex of verification.

**Mitigation strategies:** Cross-reference with authoritative sources, ask the same question to multiple tools, request URLs for all claims, maintain healthy skepticism toward overly smooth or confident answers, and when in doubt, check with Ivan.

### Context Window
**Definition:** The maximum amount of text (measured in tokens) that an LLM can "see" at once. Everything beyond the window is invisible to the model.

**Why it matters:** Long Cline sessions degrade because the context window fills with earlier conversation, leaving less room for your actual research. You will learn to recognize the signs — repetition, forgetting earlier instructions, shallow answers — and start fresh sessions.

---

## 3. LLM Model Ecosystem

### Large Language Model (LLM)
**Definition:** A neural network trained on vast text corpora to predict the next token in a sequence. Through scale and training, LLMs develop emergent capabilities including reasoning, translation, summarization, code generation, and conversational interaction.

**Why it matters:** Understanding what an LLM *is* (and is not) shapes how you use it. It is not a database. It is not a search engine. It is not a reasoning engine in the human sense. It is a pattern-completion machine that happens to produce useful outputs when prompted well — and misleading outputs when prompted poorly or asked about things outside its training distribution.

### Model Families and Providers
**Definition:** Different organizations build different LLMs with different architectures, training data, and capabilities. Key families include Claude (Anthropic), GPT (OpenAI), Gemini (Google), Llama (Meta, open-source), and Mistral (European, open-source).

**Why it matters:** Cline, KiloCode, and Zed Agent may use different underlying models. Each has different strengths, weaknesses, knowledge cutoffs, and behavioral tendencies. Knowing which model you are talking to helps you calibrate your trust.

**Resources:**
- [LLM Leaderboard (LMSys Chatbot Arena)](https://chat.lmsys.org/) — Community-driven model comparisons
- [Anthropic Models Overview](https://docs.anthropic.com/en/docs/about-claude/models) — Claude model family
- [OpenAI Models Overview](https://platform.openai.com/docs/models) — GPT model family

### Token
**Definition:** The basic unit of text that LLMs process — roughly 0.75 words in English. Models charge by token and have token limits (context windows).

**Why it matters:** You will encounter token limits in long research sessions. Knowing that ~1,000 tokens ≈ 750 words helps you estimate when you are approaching limits.

### Training Data Cutoff
**Definition:** The date after which an LLM has no knowledge. Events, papers, regulations, and tools released after this date are invisible to the model unless supplemented by tool use, search, or your own input.

**Why it matters:** Cline may not know about the latest Swiss food safety regulation or the most recent Ethereum improvement proposal. You are the bridge between the model's static knowledge and the live world. When researching temporal change in your domain, verify recency explicitly.

---

## 4. MCP Tools & Agent Skills

### Model Context Protocol (MCP)
**Definition:** An open protocol (introduced by Anthropic in 2024) that standardizes how AI agents connect to external tools, data sources, and services. MCP servers expose tools that agents can call — file systems, databases, APIs, web search, and more.

**Why it matters:** When Cline reads your files, runs terminal commands, or searches the web, it is likely using MCP under the hood. Understanding MCP helps you understand what your AI tools can and cannot reach. During the internship, you may build or configure MCP tools to extend your agent's capabilities.

**Resources:**
- [Model Context Protocol Specification](https://modelcontextprotocol.io/) — Official spec and documentation
- [MCP Servers Directory](https://github.com/modelcontextprotocol/servers) — Community-built MCP servers

### Agent Skill
**Definition:** A reusable prompt template or tool configuration that extends an AI agent's capabilities for a specific task. Skills can be shared, versioned, and composed.

**Why it matters:** During the program, you will build agent skills — for scraping research papers, for formatting curation-ready markdown, for self-administering grill-me interrogations. Skills are how you amplify your AI tools beyond their defaults. They are also artifacts you can share with the other intern or carry forward after the program.

### Tool Use / Function Calling
**Definition:** The capability of an LLM to invoke external functions — run code, query a database, search the web, read a file — rather than relying solely on its training data.

**Why it matters:** Tool use is what transforms an LLM from a chatbot into a research agent. When Cline reads your CSV, it is using a tool. When it searches for Swiss food regulations, it is using a tool. The boundary between model knowledge and tool-mediated knowledge is where research depth lives.

---

## 5. ACP & A2A Agent Protocols

### Agent Communication Protocol (ACP)
**Definition:** A proposed standard for how AI agents communicate with each other — passing tasks, sharing context, negotiating capabilities, and coordinating workflows.

**Why it matters:** ACP is bleeding-edge (as of mid-2026). Understanding it — even at a conceptual level — puts you ahead of the curve. During the internship, you may encounter ACP when multiple agents (e.g., Cline + a specialized research agent) need to coordinate on a complex task.

### Agent-to-Agent (A2A) Protocol
**Definition:** Google's protocol for agent interoperability, designed to let agents from different ecosystems discover each other, negotiate capabilities, and collaborate on tasks without human intermediation at every step.

**Why it matters:** Like ACP, A2A represents the frontier of agent infrastructure. Understanding agent-to-agent communication helps you think about the difference between using one AI tool and orchestrating multiple AI tools working together — a distinction that becomes relevant when you are using Cline, KiloCode, and Zed Agent simultaneously.

**Resources:**
- [Google A2A Protocol](https://developers.google.com/agent-to-agent) — Official documentation
- Search for "ACP agent communication protocol" in Cline — this is a fast-moving space

### Agent Orchestration
**Definition:** The practice of coordinating multiple AI agents to accomplish a complex task that no single agent could handle alone. Includes task decomposition, agent selection, result aggregation, and conflict resolution.

**Why it matters:** As you adopt multiple AI tools, you become — intentionally — an agent orchestrator. You decompose your research into subtasks, route them to the right tool, evaluate competing outputs, and synthesize results. This is a meta-skill that transcends any specific tool.

---

## 6. AI Workflow Transformation

### Workflow Automation
**Definition:** The use of technology to execute recurring tasks, decisions, or processes with minimal human intervention. AI extends automation into domains previously requiring human judgment — writing, analysis, coding, research synthesis.

**Why it matters:** You are living this transformation. Before AI tools, a literature review on Swiss fermentation would take weeks of manual searching, reading, and note-taking. With AI, you can survey the landscape in hours. But the speed creates new challenges: verification burden increases, depth can suffer, and the temptation to accept AI outputs without scrutiny grows. Understanding the transformation is part of developing responsible AI literacy.

### Human-in-the-Loop
**Definition:** A system design pattern where AI automates routine work but humans remain in the decision chain for judgment, verification, and ethical oversight.

**Why it matters:** Your internship is a human-in-the-loop research process. AI generates, you evaluate. AI synthesizes, you verify. AI drafts, you curate. The research professionals are a second loop. The pattern is: AI proposes, human disposes. Learning to inhabit this role — neither blindly trusting nor reflexively rejecting — is the core of AI literacy.

### Augmentation vs. Automation
**Definition:** Automation replaces human work. Augmentation enhances human capability. Most AI tools are best understood as augmentations — they make you faster, broader, and more capable, but they do not replace your judgment.

**Why it matters:** Your goal is augmentation, not automation. You are not trying to build a bot that does research without you. You are trying to use AI to amplify your own curiosity, speed, and depth. The deliverable is yours — the AI was a tool you wielded, not a co-author.

**Resources:**
- [Ethan Mollick — "Co-Intelligence"](https://www.penguinrandomhouse.com/books/741407/co-intelligence-by-ethan-mollick/) — Book on AI as a thinking partner
- [One Useful Thing (Mollick's Substack)](https://www.oneusefulthing.org/) — Practical AI research and advice

---

## 7. Deterministic vs. Probabilistic Compute

### Deterministic Computing
**Definition:** A system where the same input always produces the same output. Traditional software — calculators, compilers, databases — is deterministic. `2 + 2` always equals `4`. A SQL query on unchanged data always returns the same result.

### Probabilistic Computing
**Definition:** A system where the same input may produce different outputs. LLMs are probabilistic: the same prompt, issued twice, can yield different responses. This is not a flaw — it is inherent to how these models work (token-by-token prediction from probability distributions).

**Why it matters:** This distinction is the foundation of AI literacy. When you ask Cline a question and get an answer, you are not querying a database — you are sampling from a probability distribution over plausible completions. The answer *sounds* authoritative because the model was trained on authoritative text, not because it *is* authoritative. Understanding this distinction — deterministic vs. probabilistic — is what separates someone who uses AI from someone who is AI-literate.

### Temperature
**Definition:** A parameter controlling the "creativity" of LLM output. Low temperature (0.0-0.3) produces more deterministic, focused output. High temperature (0.7-1.0) produces more varied, creative, and sometimes hallucinatory output.

**Why it matters:** For research tasks that require factual accuracy, lower temperature is generally better. For brainstorming and exploration, higher temperature can be useful. You may not control temperature directly in Cline, but understanding it helps you diagnose why certain sessions feel more "creative" or "unreliable" than others.

### Verification Reflex
**Definition:** The habit of automatically checking AI-generated claims against authoritative sources, rather than accepting them at face value.

**Why it matters:** This is the single most important AI literacy skill you will build this summer. Every time Cline makes a factual claim, your internal alarm should trigger: *can I verify this?* Build the reflex early. It will serve you long after the internship ends.

---

## Quick Reference: The 7 Literacy Areas

| # | Area | Core Concept | One-Sentence Test |
|---|------|-------------|-------------------|
| 1 | Git & GitHub | Version control and collaboration | Can you branch, commit, push, and open a PR? |
| 2 | LLM Prompting | Designing effective inputs for language models | Can you write a prompt that produces a specific, verifiable, well-structured research output? |
| 3 | LLM Ecosystem | Model families, capabilities, and limitations | Can you identify which model you are talking to and calibrate your trust accordingly? |
| 4 | MCP & Agent Skills | Tool-use protocols and reusable agent capabilities | Can you configure or build a tool that extends what your AI agent can do? |
| 5 | ACP & A2A | Agent-to-agent communication standards | Can you explain how multiple AI agents coordinate on a task? |
| 6 | Workflow Transformation | How AI reshapes work processes | Can you articulate what changed in your own research workflow because of AI? |
| 7 | Deterministic vs. Probabilistic | The fundamental nature of LLMs | If Cline gives two different answers to the same question, do you understand *why*? |

---

**Note:** This dictionary is a starting point, not a textbook. The best way to learn these concepts is to encounter them in practice — when Cline hallucinates a Swiss regulation, you will understand hallucination viscerally. When two tools disagree, you will understand probabilistic compute through experience. Return to this document when a concept surfaces in your work; the definitions will mean more each time you read them.
