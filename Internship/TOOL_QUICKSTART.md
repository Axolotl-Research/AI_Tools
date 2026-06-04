---
title: "Tool Quickstart — GitHub, Cline, Zed, KiloCode"
audience: [interns]
last_updated: 2026-06-03
version: "1.0.0"
status: "Active"
domain: "Internship Program Management"
---

# Tool Quickstart Guide

**Purpose:** The minimum you need to know to get started with each tool in Week 1. This is not a manual — it is an unblocker. For depth, ask Cline.

---

## GitHub — Your Ground Truth

GitHub is where everything lives. If it is not pushed to GitHub, it does not exist.

### What You Must Be Able To Do (Week 1)

```bash
# Clone your repo (replace "your-repo-name" with your actual repository name)
git clone https://github.com/Axolotl-Research/your-repo-name.git
cd your-repo-name

# Create a branch for your work (replace "week1-research" with a descriptive branch name)
git checkout -b week1-research

# Check what you have changed
git status

# Stage and commit your work
git add research/my-first-artifact.md
git commit -m "Initial research on lacto-fermentation taxonomy"

# Push to GitHub
git push origin week1-research

# (Optional) Open a pull request on GitHub.com if you want review before merging

# Merge your branch when ready
git checkout main
git merge week1-research
git push origin main
```

### Key Concepts

| Concept | What It Means |
|---------|---------------|
| **Repository (repo)** | A folder that Git tracks. Your entire internship lives in one repo. |
| **Commit** | A snapshot of your work at a point in time. Write clear commit messages. |
| **Push** | Upload your commits to GitHub (makes them visible to the research team). |
| **Pull** | Download changes from GitHub (if someone else committed, or you worked from another machine). |
| **Branch** | A parallel version of your work. Use branches to experiment without breaking your main line. |
| **Pull Request (PR)** | A request to merge your branch into main. The research team can review and comment before merging. |
| **`.gitignore`** | A file that tells Git which files NOT to track (e.g., `.db` files, API keys, node_modules). Create one early. |

### Your First `.gitignore`

```gitignore
# Never commit these:
*.db
*.sqlite
*.sqlite3
.env
node_modules/
__pycache__/
*.pyc
.DS_Store
```

### Where to Learn More

- [GitHub Skills](https://skills.github.com/) — Interactive courses (free)
- [Oh My Git!](https://ohmygit.org/) — A game that teaches Git
- Ask Cline: "Teach me how to resolve a merge conflict in Git"

---

## Cline — Your Primary AI Research Partner

Cline is an AI coding agent that lives in your development environment (VS Code or compatible editor). It can read your files, write code, run terminal commands, and research topics with you.

### What You Must Be Able To Do (Week 1)

1. **Start a conversation.** Open Cline in your editor and type a prompt.
2. **Give it context.** Use `@` to reference files in your repo so Cline knows what you are working on.
3. **Iterate.** Cline's first answer is rarely the best one. Ask follow-ups. Push back. Say "that is wrong — try again."
4. **Verify.** Cline is probabilistic, not deterministic. It will hallucinate. Check its claims against other sources.

### Effective Prompting Patterns

| Pattern | Example | Why It Works |
|---------|---------|-------------|
| **Role + Task + Format** | "You are a food scientist. Explain the difference between lacto-fermentation and acetic acid fermentation in 3 bullet points, with examples from Swiss cuisine." | Gives Cline a stance, a specific deliverable, and a format constraint |
| **Chain of thought** | "Walk me through the steps to deploy an ERC-20 token on Ethereum Sepolia testnet. At each step, explain what could go wrong." | Forces Cline to reason step-by-step rather than giving a surface answer |
| **Verify and correct** | "You said Lactobacillus is the only bacteria in kimchi. That is wrong — Leuconostoc is also present. Acknowledge the correction and revise your explanation." | Trains Cline (within the session) to be more accurate |
| **Source request** | "List 5 Swiss food research institutions that study fermentation. For each, provide a URL to their official website." | Anchors Cline's output to verifiable sources |
| **Constraint framing** | "Summarize the ERC-721 standard in under 200 words. Focus only on the ownership model, not the technical implementation." | Prevents rambling; forces precision |

### What Cline Is Bad At (And What To Do)

| Weakness | Mitigation |
|----------|-----------|
| **Hallucinating facts** | Always verify claims with a second source. If Cline cites a paper, find the paper. |
| **Overconfidence** | Cline rarely says "I do not know." When it should. If an answer feels too smooth, probe it. |
| **Recency** | Cline's training data has a cutoff. It may not know about events, regulations, or tools from the last 6-12 months. |
| **Repetition** | When stuck, Cline sometimes loops. Break the loop by rephrasing the question or changing the format demand. |
| **Context window** | Long conversations degrade. Start fresh sessions for new research topics. |

### Where to Learn More

- [Cline Documentation](https://docs.cline.bot/) — Official docs
- [Anthropic Prompt Engineering Guide](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/overview) — Principles that apply to all LLMs
- Ask Cline: "What are the most common mistakes beginners make when prompting LLMs?"

---

## Zed Agent — Your AI-Enhanced Editor

Zed is a fast, collaborative code editor with a built-in AI agent. It is where you will write markdown, edit code, and draft artifacts.

### What You Must Be Able To Do (Week 1)

1. **Open your repo in Zed.** File → Open Folder → select your GitHub repo directory.
2. **Use the AI agent.** Open the agent panel and type a prompt. The agent can read your open files and suggest edits.
3. **Write and preview markdown.** Zed has a built-in markdown preview. Use it to check your artifact formatting.
4. **Accept or reject AI suggestions.** The agent proposes edits — you decide whether to accept them.

### Zed-Specific Tips

- **Inline assistant:** Select text and press `Ctrl+Enter` (or `Cmd+Enter` on Mac) to ask the AI about the selection.
- **Multiple files:** The agent can see your open files. Keep related files open when asking for cross-file changes.
- **Markdown preview:** `Ctrl+Shift+M` (or `Cmd+Shift+M`) to toggle preview. Use it constantly.
- **Skills:** Zed supports agent skills — reusable prompt templates. You will learn to build these during the program.

### Where to Learn More

- [Zed Documentation](https://zed.dev/docs) — Official docs
- Ask the Zed Agent: "Show me how to use skills in Zed"

---

## KiloCode — Your Second AI Agent

KiloCode (kilo.ai) is an AI coding agent similar to Cline. You will adopt it as your needs evolve — not necessarily in Week 1.

### What You Must Be Able To Do (When You Start)

1. **Know that it exists.** You have an account. You can log in when ready.
2. **Understand the overlap.** KiloCode and Cline do similar things. This is a feature, not a bug — when they disagree, you learn.
3. **Compare outputs.** Try the same prompt in both tools. Note the differences. Develop your judgment about which answer is better and why.

### When to Use KiloCode Instead of Cline

- Cline is stuck in a loop and a fresh perspective would help
- You want to compare two AI-generated approaches to the same problem
- You are building something that KiloCode handles better (you will discover this through experimentation)
- You want to verify Cline's claims by getting a second AI opinion

### Where to Learn More

- [KiloCode Documentation](https://kilo.ai/docs) — Official docs (verify URL if broken; search "KiloCode documentation" as fallback)
- Ask KiloCode: "How are you different from other AI coding agents?"

---

## General Advice for All AI Tools

1. **You are the arbiter.** The AI is a tool, not an authority. If something feels wrong, it probably is.
2. **Commit before asking AI to make changes.** That way you can always revert.
3. **Start new sessions for new topics.** Long conversations degrade. Fresh context produces better results.
4. **The prompt is a skill.** Your first 50 prompts will be mediocre. Your 500th will be sharp. That is the learning curve.
5. **When in doubt, WhatsApp the group.**
