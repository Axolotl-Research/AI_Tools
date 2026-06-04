---
title: "AI & Research Literacy — Curated Resource Links"
audience: [interns]
last_updated: 2026-06-03
version: "1.0.0"
status: "Active"
domain: "Internship Program Management"
---

# Curated Resource Links

**Purpose:** A standalone collection of the best free resources for each AI literacy area. Use this as your launchpad — open links, follow threads, go deep on what interests you. This file is meant to grow as you discover resources during your research.

**Link tiers:** 🟢 = beginner (start here) | 🟡 = intermediate (go deeper) | 🔴 = advanced / academic

---

## 1. Git & GitHub Basics

### Interactive Learning
- 🟢 [GitHub Skills](https://skills.github.com/) — Free interactive courses from GitHub; start with "Introduction to GitHub"
- 🟢 [Oh My Git!](https://ohmygit.org/) — A visual game that teaches Git internals through play
- 🟢 [Learn Git Branching](https://learngitbranching.js.org/) — Visual, interactive Git branching tutorial
- 🟡 [Git Immersion](https://gitimmersion.com/) — Guided tour of Git fundamentals through hands-on labs

### Documentation & Reference
- 🟢 [GitHub Docs: Get Started](https://docs.github.com/en/get-started) — Official GitHub getting-started guide
- 🟡 [Atlassian Git Tutorials](https://www.atlassian.com/git/tutorials) — Comprehensive written guides from beginner to advanced
- 🔴 [Pro Git Book](https://git-scm.com/book/en/v2) — The definitive Git reference by Scott Chacon and Ben Straub (free online)
- 🟢 [Git Cheat Sheet (GitHub)](https://education.github.com/git-cheat-sheet-education.pdf) — Printable one-page reference

### Specific Skills
- 🟢 [GitHub Flow Guide](https://docs.github.com/en/get-started/using-github/github-flow) — How to use branches and pull requests
- 🟡 [Resolving Merge Conflicts](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/addressing-merge-conflicts/resolving-a-merge-conflict-on-github) — When things go wrong
- 🟢 [Writing Good Commit Messages](https://cbea.ms/git-commit/) — The classic guide by Chris Beams
- 🟢 [Conventional Commits](https://www.conventionalcommits.org/) — A standard format for commit messages
- 🟡 [GitHub Markdown Guide](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax) — Formatting your README and artifacts
- 🟡 [Mermaid Diagrams in GitHub Markdown](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/creating-diagrams) — How ER diagrams render on GitHub

### Tools
- 🟢 [GitHub Desktop](https://desktop.github.com/) — Visual Git client (if the command line is intimidating)
- 🟡 [GitLens (VS Code Extension)](https://marketplace.visualstudio.com/items?itemName=eamodio.gitlens) — Git superpowers inside your editor

---

## 2. LLM Prompting

### Prompt Engineering Guides
- 🟢 [Anthropic Prompt Engineering Guide](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/overview) — Excellent, tool-agnostic principles from the makers of Claude
- 🟡 [OpenAI Prompt Engineering Guide](https://platform.openai.com/docs/guides/prompt-engineering) — Six strategies for better results
- 🟡 [Prompt Engineering Guide (DAIR.AI)](https://www.promptingguide.ai/) — Comprehensive community-maintained resource
- 🟢 [Google: Prompt Design Strategies](https://ai.google.dev/gemini-api/docs/prompting-strategies) — Gemini-focused but widely applicable

### Prompt Libraries & Examples
- 🔴 [Anthropic Prompt Library](https://docs.anthropic.com/en/prompt-library/library) — Real-world prompt examples for Claude
- 🟡 [OpenAI Cookbook](https://cookbook.openai.com/) — Prompt techniques and code examples
- 🟢 [Awesome ChatGPT Prompts](https://github.com/f/awesome-chatgpt-prompts) — Community-curated prompt collection

### Advanced Techniques
- 🟡 [Chain-of-Thought Prompting (arXiv)](https://arxiv.org/abs/2201.11903) — The paper that introduced chain-of-thought
- 🟡 [Anthropic: Using Long Context](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/long-context-tips) — Prompting with large context windows
- 🟡 [Lilian Weng: Prompt Engineering](https://lilianweng.github.io/posts/2023-03-15-prompt-engineering/) — Deep technical overview
- 🔴 [Brex Prompt Engineering Guide](https://github.com/brexhq/prompt-engineering) — Hard-won lessons from production use

### Hallucination
- 🟢 [Wikipedia: Hallucination (AI)](https://en.wikipedia.org/wiki/Hallucination_(artificial_intelligence)) — Overview of the phenomenon
- 🟡 [Anthropic: Reducing Hallucinations](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/reduce-hallucinations) — Practical strategies
- 🔴 [Survey of Hallucination in LLMs (arXiv)](https://arxiv.org/abs/2311.05232) — Academic survey of the problem

---

## 3. LLM Model Ecosystem

### Understanding How LLMs Work
- 🟢 [3Blue1Brown: How LLMs Work (video)](https://www.youtube.com/watch?v=wjZofJX0v4M) — Visual explanation of transformers and attention
- 🟢 [3Blue1Brown: Attention in Transformers (video)](https://www.youtube.com/watch?v=eMlx5fFNoYc) — Visual deep-dive into the attention mechanism
- 🟡 [Andrej Karpathy: Intro to LLMs (video)](https://www.youtube.com/watch?v=zjkBMFhNj_g) — Deep dive by a leading AI researcher
- 🟡 [Andrej Karpathy: Let's Build GPT from Scratch (video)](https://www.youtube.com/watch?v=kCc8FmEb1nY) — Code-along building of a transformer
- 🟡 [Stephen Wolfram: What Is ChatGPT Doing?](https://writings.stephenwolfram.com/2023/02/what-is-chatgpt-doing-and-why-does-it-work/) — Detailed, accessible explanation
- 🟢 [Anthropic: How Claude Thinks (blog)](https://www.anthropic.com/research) — Anthropic's research blog on model behavior
- 🔴 [Attention Is All You Need (arXiv)](https://arxiv.org/abs/1706.03762) — The original transformer paper (2017)

### Model Comparisons & Benchmarks
- 🟢 [LMSys Chatbot Arena](https://chat.lmsys.org/) — Community-driven blind model comparisons
- 🟡 [Artificial Analysis](https://artificialanalysis.ai/) — Independent model benchmarks (speed, quality, price)
- 🟡 [Hugging Face Open LLM Leaderboard](https://huggingface.co/spaces/open-llm-leaderboard/open_llm_leaderboard) — Benchmarks for open-source models
- 🔴 [Papers With Code: NLP Benchmarks](https://paperswithcode.com/area/natural-language-processing) — Academic benchmarks and state-of-the-art

### Model Providers & Documentation
- 🟡 [Anthropic Models Overview](https://docs.anthropic.com/en/docs/about-claude/models) — Claude model family (likely what powers Cline)
- 🟡 [OpenAI Models Overview](https://platform.openai.com/docs/models) — GPT model family
- 🟡 [Google Gemini Models](https://ai.google.dev/gemini-api/docs/models) — Gemini model family
- 🟡 [Meta Llama](https://llama.meta.com/) — Open-source model family
- 🟡 [Mistral AI](https://mistral.ai/) — European open-source models
- 🟡 [Hugging Face Models](https://huggingface.co/models) — Repository of thousands of open models

### Key Concepts
- 🟢 [OpenAI Tokenizer](https://platform.openai.com/tokenizer) — Interactive tool: see how text breaks into tokens
- 🟡 [Anthropic: Context Windows](https://docs.anthropic.com/en/docs/build-with-claude/context-windows) — Understanding and working with context limits
- 🟡 [Hugging Face NLP Course](https://huggingface.co/learn/nlp-course) — Free course on modern NLP (includes transformers, tokenization, fine-tuning)

---

## 4. MCP Tools & Agent Skills

### Model Context Protocol (MCP)
- 🟢 [MCP Introduction](https://modelcontextprotocol.io/introduction) — Official intro: what MCP is and why it matters
- 🟡 [MCP Specification](https://modelcontextprotocol.io/) — Full protocol specification
- 🟡 [MCP Quickstart Guide](https://modelcontextprotocol.io/quickstart) — Build your first MCP server
- 🟡 [MCP Servers Directory](https://github.com/modelcontextprotocol/servers) — Community-built MCP servers (filesystem, GitHub, web search, databases, and more)
- 🟡 [MCP Architecture](https://modelcontextprotocol.io/docs/concepts/architecture) — How MCP works under the hood
- 🟡 [Building MCP Servers (Python)](https://modelcontextprotocol.io/quickstart/server) — Python SDK tutorial
- 🟡 [Building MCP Servers (TypeScript)](https://github.com/modelcontextprotocol/typescript-sdk) — TypeScript SDK
- 🔴 [Anthropic: Introducing MCP (blog)](https://www.anthropic.com/news/model-context-protocol) — The announcement and vision

### Agent Skills
- 🟢 [Zed Agent Skills Documentation](https://zed.dev/docs/assistant-panel) — How skills work in Zed
- 🟡 [Zed Skills Examples](https://github.com/zed-industries/zed/tree/main/assets/skills) — Official example skills in the Zed repo
- 🟢 Ask Cline: "What are agent skills and how do I create one?"
- 🟢 Ask KiloCode: "Show me how agent skills work in KiloCode"

### Tool Use & Function Calling
- 🟡 [Anthropic: Tool Use Guide](https://docs.anthropic.com/en/docs/build-with-claude/tool-use) — How Claude uses tools
- 🟡 [OpenAI: Function Calling Guide](https://platform.openai.com/docs/guides/function-calling) — GPT function calling
- 🟡 [LangChain Tools](https://python.langchain.com/docs/concepts/tools/) — The LangChain framework's tool abstraction

---

## 5. ACP & A2A Agent Protocols

### Agent-to-Agent (A2A) — Google
- 🟢 [Google A2A Protocol](https://developers.google.com/agent-to-agent) — Official documentation and overview
- 🟡 [A2A GitHub Repository](https://github.com/google/A2A) — Open-source implementation and examples
- 🟡 [Google: Introducing A2A (blog)](https://developers.googleblog.com/en/a2a-a-new-era-of-agent-interoperability/) — The announcement and vision

### Agent Communication Protocol (ACP)
- 🟡 Ask Cline: "Explain the Agent Communication Protocol and its relationship to MCP"
- 🟢 Ask KiloCode: "What is ACP and how does it differ from A2A?"
- 🔴 This is a fast-moving space in mid-2026 — use AI tools to stay current

### Agent Orchestration & Multi-Agent Systems
- 🟡 [LangGraph](https://langchain-ai.github.io/langgraph/) — Framework for building multi-agent workflows
- 🟡 [CrewAI](https://docs.crewai.com/) — Framework for orchestrating role-playing AI agents
- 🟡 [AutoGen (Microsoft)](https://microsoft.github.io/autogen/) — Multi-agent conversation framework
- 🔴 [Anthropic: Building Effective Agents (blog)](https://www.anthropic.com/research/building-effective-agents) — Design patterns for agent systems

### Agent Standards & Interoperability
- 🟡 [OpenAI Agents SDK](https://openai.github.io/openai-agents-python/) — OpenAI's agent framework
- 🟡 [Agent Protocol (LangChain)](https://github.com/langchain-ai/agent-protocol) — Standardized agent API
- 🔴 This space is evolving rapidly — use Cline weekly to check for new standards

---

## 6. AI Workflow Transformation

### Books & Long-Form
- 🟢 [Ethan Mollick — Co-Intelligence: Living and Working with AI](https://www.penguinrandomhouse.com/books/741407/co-intelligence-by-ethan-mollick/) — Best book on AI as a thinking partner
- 🟡 [Mustafa Suleyman — The Coming Wave](https://www.the-coming-wave.com/) — AI's impact on society, power, and work
- 🟡 [Arvind Narayanan & Sayash Kapoor — AI Snake Oil](https://www.aisnakeoil.com/) — What AI can and cannot do

### Newsletters & Blogs
- 🟢 [One Useful Thing (Ethan Mollick)](https://www.oneusefulthing.org/) — Practical AI research and advice
- 🟡 [The Batch (Andrew Ng / DeepLearning.AI)](https://www.deeplearning.ai/the-batch/) — Weekly AI news and insights
- 🟡 [Import AI (Jack Clark)](https://jack-clark.net/) — Weekly newsletter on AI research and policy
- 🟡 [Stratechery (Ben Thompson)](https://stratechery.com/) — Tech strategy, including AI's business impact
- 🟡 [Anthropic Research Blog](https://www.anthropic.com/research) — Research from the makers of Claude
- 🟡 [OpenAI Research Blog](https://openai.com/research/) — Research from OpenAI
- 🟡 [Google DeepMind Blog](https://deepmind.google/discover/blog/) — Research from DeepMind

### AI's Impact on Specific Domains
- 🟡 [AI in Food Science (Frontiers)](https://www.frontiersin.org/journals/artificial-intelligence) — Open-access journal with food science AI papers
- 🟡 [AI in Finance / DeFi](https://arxiv.org/list/cs.AI/recent) — Search arXiv for "DeFi" + "machine learning"
- 🟡 [Swiss AI Research](https://www.ai.ethz.ch/) — ETH Zürich AI Center
- 🟡 [EPFL AI Center](https://ai.epfl.ch/) — EPFL (Lausanne) AI research

### Human-in-the-Loop & Augmentation
- 🟡 [Ethan Mollick: "The Future of Work" (talk)](https://www.youtube.com/watch?v=X4o4n1YcQqQ) — How AI changes professional work
- 🟡 [Harvard Business Review: AI Augmentation](https://hbr.org/topic/artificial-intelligence) — HBR's AI collection
- 🔴 [Microsoft Research: Human-AI Interaction](https://www.microsoft.com/en-us/research/theme/human-ai-interaction/) — Academic research on human-AI collaboration

---

## 7. Deterministic vs. Probabilistic Compute

### Foundational Explanations
- 🟢 [3Blue1Brown: But What Is a GPT? (video)](https://www.youtube.com/watch?v=wjZofJX0v4M) — Visual intuition for how LLMs work (probabilistic prediction)
- 🟡 [Stephen Wolfram: What Is ChatGPT Doing?](https://writings.stephenwolfram.com/2023/02/what-is-chatgpt-doing-and-why-does-it-work/) — Deep mathematical but accessible explanation
- 🟢 [Google: Introduction to LLMs](https://developers.google.com/machine-learning/resources/intro-llms) — Beginner-friendly ML course module
- 🟡 [Jay Alammar: The Illustrated Transformer](https://jalammar.github.io/illustrated-transformer/) — Visual guide to transformer architecture

### Probability & Statistics for AI
- 🟢 [Khan Academy: Probability](https://www.khanacademy.org/math/statistics-probability) — Free probability fundamentals
- 🟡 [Seeing Theory](https://seeing-theory.brown.edu/) — Visual introduction to probability and statistics (Brown University)
- 🟡 [3Blue1Brown: Bayes Theorem (video)](https://www.youtube.com/watch?v=HZGCoVF3YvM) — The probabilistic reasoning behind ML

### Deterministic vs. Non-Deterministic Systems
- 🟢 [Wikipedia: Deterministic Algorithm](https://en.wikipedia.org/wiki/Deterministic_algorithm) — What "deterministic" means
- 🟢 [Wikipedia: Nondeterministic Algorithm](https://en.wikipedia.org/wiki/Nondeterministic_algorithm) — The contrast
- 🟡 [Andrej Karpathy: "LLMs Are Not Databases" (talk excerpt)](https://www.youtube.com/watch?v=cdiD-9MMpb0) — Why you cannot query an LLM like a database

### Temperature, Sampling & Generation
- 🟡 [OpenAI: How Temperature Works](https://platform.openai.com/docs/guides/text-generation/how-should-i-set-the-temperature-parameter) — Practical guide to the temperature parameter
- 🟡 [Anthropic: Controlling Model Output](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/control-output) — Temperature, top-p, and other controls
- 🔴 [Hugging Face: How to Generate Text](https://huggingface.co/blog/how-to-generate) — Decoding strategies (greedy, beam search, sampling)

---

## 8. Entity-Relationship Modeling & Semantic Spaces

### Entity-Relationship Diagrams
- 🟢 [Mermaid ER Diagram Guide](https://mermaid.js.org/syntax/entityRelationshipDiagram.html) — The syntax you will use
- 🟢 [Mermaid Live Editor](https://mermaid.live/) — Draw and preview diagrams in your browser
- 🟡 [Wikipedia: Entity-Relationship Model](https://en.wikipedia.org/wiki/Entity%E2%80%93relationship_model) — The concept behind the diagrams
- 🟡 [Lucidchart: ER Diagram Tutorial](https://www.lucidchart.com/pages/er-diagrams) — Visual guide to ER diagram symbols and notation
- 🟡 [Visual Paradigm: ERD Guide](https://www.visual-paradigm.com/guide/data-modeling/what-is-entity-relationship-diagram/) — Comprehensive ERD tutorial

### Mermaid (Diagramming Tool)
- 🟢 [Mermaid Documentation](https://mermaid.js.org/intro/) — Full documentation
- 🟢 [Mermaid Cheat Sheet](https://jojozhuang.github.io/tutorial/mermaid-cheat-sheet/) — Quick reference
- 🟡 [Mermaid in GitHub Markdown](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/creating-diagrams) — How to embed mermaid in your README
- 🟡 [Mermaid in Zed](https://zed.dev/docs/languages/mermaid) — Zed's native mermaid support

### Semantic Web & Knowledge Representation
- 🟡 [W3C RDF Primer](https://www.w3.org/TR/rdf11-primer/) — Introduction to the Resource Description Framework
- 🟡 [W3C Turtle Specification](https://www.w3.org/TR/turtle/) — The Turtle RDF syntax
- 🟡 [DBpedia](https://www.dbpedia.org/) — Structured data extracted from Wikipedia (see Turtle/RDF in action)
- 🟡 [Wikidata](https://www.wikidata.org/) — Free knowledge base; explore entity-relationship structures at scale
- 🔴 [Schema.org](https://schema.org/) — Shared vocabulary for structured data on the web
- 🔴 [Tim Berners-Lee: The Semantic Web (Scientific American)](https://www-sop.inria.fr/acacia/cours/essi2006/Scientific%20American_%20Feature%20Article_%20The%20Semantic%20Web_%20May%202001.pdf) — The original vision (2001)

### Domain Modeling & Ontologies
- 🟡 [Domain-Driven Design Quickly (free book)](https://www.infoq.com/minibooks/domain-driven-design-quickly/) — Introduction to domain modeling concepts
- 🟡 [Ontology Engineering 101 (Stanford)](https://protege.stanford.edu/publications/ontology_development/ontology101.pdf) — Guide to building ontologies (the academic cousin of ER diagrams)
- 🔴 [Protégé (Stanford)](https://protege.stanford.edu/) — Free ontology editor (advanced)

---

## 9. General AI & Research Methodology

### AI Literacy (Broad)
- 🟢 [Elements of AI](https://www.elementsofai.com/) — Free online course from the University of Helsinki (no math prerequisite)
- 🟢 [Google: AI for Everyone](https://www.coursera.org/learn/ai-for-everyone) — Andrew Ng's accessible AI introduction
- 🟡 [fast.ai Practical Deep Learning](https://course.fast.ai/) — Hands-on deep learning course (requires some coding)
- 🟡 [DeepLearning.AI Short Courses](https://www.deeplearning.ai/short-courses/) — Free short courses on specific AI topics

### Research Methodology
- 🟢 [Purdue OWL: Research Overview](https://owl.purdue.edu/owl/research_and_citation/conducting_research/index.html) — How to conduct academic research
- 🟢 [SAGE Research Methods](https://methods.sagepub.com/) — Comprehensive research methods resource
- 🟡 [Google Scholar](https://scholar.google.com/) — Search academic papers across disciplines
- 🟡 [PubMed](https://pubmed.ncbi.nlm.nih.gov/) — Biomedical literature (for food science / fermentation research)
- 🟡 [arXiv](https://arxiv.org/) — Preprint server for computer science, economics, quantitative biology
- 🟡 [SSRN](https://www.ssrn.com/) — Social science and economics preprints (for crypto/finance research)

### Swiss-Specific Research Resources
- 🟡 [Agroscope](https://www.agroscope.admin.ch/) — Swiss federal research center for agriculture and food
- 🟡 [ETH Zürich Research Collection](https://www.research-collection.ethz.ch/) — ETH Zürich's institutional repository
- 🟡 [EPFL Infoscience](https://infoscience.epfl.ch/) — EPFL's institutional repository
- 🟡 [Swiss National Science Foundation](https://www.snf.ch/) — Funding and research database
- 🟡 [Swiss Federal Food Safety and Veterinary Office](https://www.blv.admin.ch/) — Food safety regulations and research
- 🟡 [Swiss Biotech Association](https://www.swissbiotech.org/) — Swiss biotech industry (includes food tech)
- 🟡 [Swiss Finance Institute](https://www.sfi.ch/) — Financial research (for crypto/tokenization context)
- 🟡 [FINMA](https://www.finma.ch/) — Swiss financial market supervisory authority (crypto regulation)
- 🟡 [ZHAW Food Technology](https://www.zhaw.ch/en/lsfm/institutes-centres/ilgi/food-technology/) — Zürich University of Applied Sciences food tech research

### AI Tools & Platforms
- 🟢 [Cline Documentation](https://docs.cline.bot/) — Official Cline docs
- 🟡 [KiloCode Documentation](https://kilo.ai/docs) — Official KiloCode docs
- 🟢 [Zed Documentation](https://zed.dev/docs) — Official Zed docs
- 🟡 [Hugging Face](https://huggingface.co/) — Platform for models, datasets, and ML community
- 🟡 [Kaggle](https://www.kaggle.com/) — Datasets, competitions, and ML learning resources
- 🟡 [Google Colab](https://colab.research.google.com/) — Free cloud notebooks for Python/ML experimentation

### AI Ethics & Safety
- 🟡 [Anthropic: Core Views on AI Safety](https://www.anthropic.com/news/core-views-on-ai-safety) — Safety philosophy from Anthropic
- 🟡 [AI Safety Fundamentals (BlueDot Impact)](https://aisafetyfundamentals.com/) — Free course on AI safety
- 🟡 [The Alignment Problem (Brian Christian)](https://brianchristian.org/the-alignment-problem/) — Book on machine learning and human values

---

## 10. Domain-Specific Resources

### Fermented Food Systems & Swiss Food Ecosystem
- 🟢 [Wikipedia: Fermentation in Food Processing](https://en.wikipedia.org/wiki/Fermentation_in_food_processing) — Broad overview
- 🟢 [FAO: Fermented Foods](https://www.fao.org/food-safety/scientific-advice/jecfa/fermented-foods/en/) — UN Food and Agriculture Organization resources
- 🟡 [Agroscope: Fermented Foods Research](https://www.agroscope.admin.ch/agroscope/en/home/topics/food.html) — Swiss federal research
- 🟡 [ETH Zürich: Food Process Engineering](https://fpe.ethz.ch/) — ETH lab for food processing
- 🟡 [ZHAW: Food Biotechnology](https://www.zhaw.ch/en/lsfm/institutes-centres/ilgi/food-biotechnology/) — Fermentation research group
- 🟡 [Bern University of Applied Sciences: Food Science](https://www.bfh.ch/en/research/research-areas/food-science/) — Swiss food science research
- 🟡 [Nestlé Research (Lausanne)](https://www.nestle.com/randd) — Major Swiss food R&D center
- 🟡 [Givaudan (Vernier)](https://www.givaudan.com/) — Swiss flavors and fragrances company (fermentation-related)
- 🟡 [Swiss Food Research](https://www.swissfoodresearch.ch/) — Industry-academia network
- 🟡 [Standards for Fermented Foods](https://www.codexalimentarius.org/) — Codex Alimentarius international food standards

### Asset Tokenization & Cryptocurrencies
- 🟢 [Ethereum Developer Documentation](https://ethereum.org/en/developers/docs/) — Official Ethereum docs (start here for token standards)
- 🟢 [Ethereum: ERC-20 Token Standard](https://ethereum.org/en/developers/docs/standards/tokens/erc-20/) — The fungible token standard
- 🟢 [Ethereum: ERC-721 NFT Standard](https://ethereum.org/en/developers/docs/standards/tokens/erc-721/) — The non-fungible token standard
- 🟢 [Ethereum: ERC-1155 Multi-Token Standard](https://ethereum.org/en/developers/docs/standards/tokens/erc-1155/) — Multi-token standard
- 🟡 [OpenZeppelin Contracts](https://docs.openzeppelin.com/contracts/) — Audited, reusable smart contract library
- 🟡 [Solidity Documentation](https://docs.soliditylang.org/) — The smart contract programming language
- 🟡 [Remix IDE](https://remix.ethereum.org/) — Browser-based Solidity development environment
- 🟡 [Ethereum Sepolia Testnet Faucet](https://sepoliafaucet.com/) — Free test ETH for development
- 🟡 [CoinGecko](https://www.coingecko.com/) — Cryptocurrency market data and research
- 🟡 [DeFi Llama](https://defillama.com/) — DeFi analytics and protocol data
- 🟡 [Messari](https://messari.io/) — Crypto research and data
- 🟡 [The Block Research](https://www.theblock.co/research) — Crypto industry research
- 🟡 [FINMA: Crypto Regulation (Switzerland)](https://www.finma.ch/en/authorisation/fintech/) — Swiss regulatory framework
- 🟡 [Swiss Blockchain Federation](https://blockchainfederation.ch/) — Swiss blockchain industry association
- 🟡 [Crypto Valley Association (Zug)](https://cryptovalley.swiss/) — Swiss crypto ecosystem hub
- 🔴 [Bank for International Settlements: Crypto Papers](https://www.bis.org/topic/fintech/crypto.htm) — International regulatory perspective

---

## How to Use This File

1. **Do not try to read everything.** This is a launchpad, not a curriculum.
2. **Follow your curiosity.** Click a link that interests you. If it leads somewhere unexpected, follow it.
3. **Add your own discoveries.** When you find a great resource during your research, add it here. This file is meant to grow.
4. **Use the tiers.** Start with 🟢 links when you are new to a topic. Graduate to 🟡 and 🔴 as your understanding deepens.
5. **Ask AI tools to evaluate resources.** "Cline, is this link still current? Is there a better resource on this topic now?"

---

**Last updated:** 2026-06-03 | **Version:** 1.0.0
**Contributions welcome.** Add resources you discover during your research.

---

## 11. YouTube Tutorials — GitHub, Zed, Cline, KiloCode

### GitHub / Git

**Highly-rated beginner courses (all free):**
- 🟢 [Programming with Mosh: Git Tutorial for Beginners](https://www.youtube.com/watch?v=8JJ101D3knE) — 1 hour, clear explanations, millions of views
- 🟢 [freeCodeCamp: Git and GitHub for Beginners - Crash Course](https://www.youtube.com/watch?v=RGOj5yH7evk) — 1 hour, hands-on, excellent production
- 🟢 [Traversy Media: Git & GitHub Crash Course](https://www.youtube.com/watch?v=SWYqp7iY_Tc) — 1 hour, practical workflow focus
- 🟢 [The Net Ninja: Git & GitHub Tutorial Series](https://www.youtube.com/playlist?list=PL4cUxeGkcC9goXbgTDQ0n_4TBzOO0ocPR) — Bite-sized videos, great for learning in chunks
- 🟢 [SuperSimpleDev: Git and GitHub Tutorial](https://www.youtube.com/watch?v=hrTQipWp6co) — Ultra-beginner-friendly, assumes zero prior knowledge
- 🟡 [Academind: Git & GitHub — Complete Guide](https://www.youtube.com/watch?v=USjZcfj8yxE) — Deeper dive, covers branching strategy

**Search for more:** `git tutorial for beginners 2025` | `github crash course` | `git explained visually`

---

### Zed Editor

**Known tutorials (Zed is newer — fewer videos exist, but these are solid):**
- 🟢 [Official Zed Channel](https://www.youtube.com/@zeddotdev) — Demos, release walkthroughs, tips from the Zed team
- 🟡 Search YouTube for: `Zed editor tutorial 2025` — The landscape changes fast; newest videos will be most accurate
- 🟡 Search YouTube for: `Zed editor vs VS Code` — Comparison videos often double as tutorials
- 🟡 Search for creators who cover Zed: **Theo - t3.gg**, **Fireship**, **ThePrimeagen**, **TJ DeVries** (Zed co-founder)

**What to search on YouTube:**
- `Zed editor getting started`
- `Zed editor AI agent tutorial`
- `Zed editor markdown preview`
- `Zed editor mermaid diagram`

---

### Cline

**Known resources (Cline is newer — the field is fast-moving):**
- 🟢 Search YouTube for: `Cline AI coding agent tutorial 2025` — New videos appear regularly; search for the official Cline channel
- 🟡 Search YouTube for: `Cline vs Copilot` or `Cline vs Cursor` — Comparison videos often show Cline workflow
- 🟡 Search for AI tool roundup channels: **AI Jason**, **Matt Wolfe**, **The AI Advantage**, **Skill Leap AI**

**What to search on YouTube:**
- `Cline AI agent setup`
- `Cline VS Code extension tutorial`
- `how to use Cline for coding`
- `Cline MCP tools tutorial`

---

### KiloCode

**Note:** KiloCode (kilo.ai) is very new as of mid-2026. There may not yet be independent YouTube tutorials. Your best resources:
- 🟢 [Official KiloCode Documentation](https://kilo.ai/docs) — Start here
- 🟡 Search YouTube for: `KiloCode tutorial` or `kilo.ai coding agent` — The video landscape may have grown since this file was written
- 🟢 Ask KiloCode itself: "Show me a tutorial on how to use you effectively"
- 🟡 Watch Cline tutorials — many AI coding agent principles transfer between tools

**What to search on YouTube:**
- `KiloCode AI agent`
- `kilo.ai review`
- `KiloCode vs Cline`

---

### General AI Coding Agent Tutorials (apply to all tools)

These channels regularly cover AI coding tools broadly — principles transfer across Cline, KiloCode, and Zed:
- 🟡 [Fireship](https://www.youtube.com/@Fireship) — Quick, dense overviews of new AI dev tools
- 🟡 [Theo - t3.gg](https://www.youtube.com/@t3dotgg) — Deep dives on AI coding workflows
- 🟡 [ThePrimeagen](https://www.youtube.com/@ThePrimeagen) — Developer perspective on AI tools
- 🟡 [Matt Wolfe](https://www.youtube.com/@mattwolfe) — Weekly AI news and tool roundups
- 🟡 [AI Jason](https://www.youtube.com/@AIJasonZ) — AI agent and automation tutorials
- 🟡 [Skill Leap AI](https://www.youtube.com/@SkillLeapAI) — Beginner-friendly AI tool tutorials

---

### Tips for Finding Good Tutorials

1. **Sort by upload date.** AI tools change fast. A video from 3 months ago may be outdated.
2. **Check the comments.** Are people saying "this still works" or "this is broken now"?
3. **Watch at 1.5x speed.** Most tutorials are paced for absolute beginners.
4. **Code along.** Watching is passive. Open the tool and follow along.
5. **Verify with docs.** If a tutorial says something that contradicts the official documentation, trust the docs.
