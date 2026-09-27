# AI Architecture
*Designing, building and governing AI solutions in the enterprise*

| | |
|---|---|
| **Duration** | 2 days, 7 hours per day |
| **Format** | Live online |
| **Language** | English |
| **Audience** | Business analysts and technical professionals |

## Course overview

This course gives business and technical professionals a shared understanding of how AI and Generative AI solutions are designed, built, secured and run in a large enterprise. The focus is on architecture: the components of an AI solution, the patterns that combine them, and the decisions and trade-offs behind each choice.

The theoretical modules are complemented by four live demonstrations on concrete banking use cases, placed so that each half-day includes one practical session, plus a short prompt-engineering demonstration inside Module 4. The demonstrations are run by the trainer and show both the behaviour of the solution and, for technical participants, the code behind it. All demonstration data is synthetic.

## Learning objectives

By the end of the course, participants will be able to:

- Explain the fundamentals of AI, Generative AI and Large Language Models, with their capabilities, limits and risks.
- Frame an AI use case and evaluate whether and how AI should be applied.
- Recognise the main architectural patterns (prompt-based, RAG, agentic) and choose the right one for a given problem.
- Evaluate and compare models and solutions with objective criteria: quality, cost, latency and risk.
- Identify the main security, privacy and compliance risks of AI systems in a banking context, and the controls that address them.
- Understand what it takes to run AI solutions in production: LLMOps, cloud platforms, integration, monitoring and cost management.

## Practical information

- The course is delivered live online. Participants need a stable internet connection, audio and a webcam.
- Demonstrations are run by the trainer: no software installation is required.
- No programming experience is required. Code is shown during the demonstrations for technical participants, but it is not needed to follow the course.

## Day 1 — From foundations to building blocks

### Morning

**Module 1. AI and Generative AI Fundamentals**  
AI, machine learning, deep learning and Generative AI: how they relate and what changed with generative models. Typical enterprise use cases in banking.

**Module 2. Designing AI-Enabled Solutions**  
When AI is the right answer, and when it is not. Framing a use case: problem, data, users, risks and success metrics. A common decision framework used throughout the course.

**Module 3. Large Language Models and Their Capabilities**  
How an LLM works at a conceptual level: tokens, context window, training and inference. Strengths, limits (hallucinations, knowledge cut-off) and risks.

**Module 4. Prompt Engineering and Prompt Management**  
Structure of an effective prompt: role, instructions, examples and output format. Structured outputs. Managing prompts as versioned, testable assets.

> **Short demo — Prompt engineering in practice**  
> Python notebook, about 25 minutes. The opening lines of customer complaints are labelled by topic and tone with three versions of the same prompt: naive, structured (role, definitions, scale, delimiters, JSON output) and few-shot. Each version is scored on a small set of expert-labelled complaints — accuracy on topic and tone, invalid answers — and two models are compared on quality, cost and latency. Prompts are handled as versioned assets; the tone label is the sentiment feature that Demo 1 uses.

> **Demo 1 — Customer complaint classification**  
> Python notebook. A synthetic export of customer complaints is explored, cleaned and used to train a triage model that predicts, at intake, whether a complaint will be resolved at first contact, resolved after investigation or escalated to the ombudsman. Exploratory analysis, missing values and outliers (from the box plot to the Mahalanobis distance), three classification algorithms compared with train/test split, cross-validation and hyper-parameter tuning, and the business reading of the results: escalation drivers, data leakage, drift and fairness. One of the inputs, the sentiment of the complaint text, is produced live by the LLM step of the short demo.

### Afternoon

**Module 5. AI Model Selection and Evaluation**  
Proprietary and open-weight models. Selection criteria: quality, latency, cost, data residency and licensing. Test sets, evaluation metrics and LLM-as-a-judge.

**Module 6. Vector Databases and Embeddings**  
What embeddings are and how they capture meaning. Semantic search, vector databases and indexing. Document chunking strategies.

**Module 7. Retrieval-Augmented Generation (RAG) Architectures**  
Why RAG. The ingestion, retrieval and generation pipeline. Grounding and source citations. Common failure modes and how to improve retrieval (hybrid search, re-ranking).

> **Demo 2 — Internal policy assistant (RAG)**  
> Python notebook, or alternatively Azure OpenAI and Azure AI Search. An assistant that answers questions on internal policies and procedures, with source citations, and a case where retrieval fails.

## Day 2 — From agents to production

### Morning

**Module 8. AI Agents and Multi-Agent Systems**  
From chatbots to agents: tools, planning and memory. Workflows versus autonomous agents. Multi-agent patterns. Human-in-the-loop controls. When agents are, and are not, the right choice.

> **Demo 3 — Credit file verification agent**  
> Python notebook. An agent checks a loan application by querying several simulated systems (customer registry, current exposure, lending policy). Step-by-step trace of its reasoning and tool calls, with a human approval step before the final outcome.

**Module 9. AI Integration with Enterprise Systems and APIs**  
Integrating LLMs through APIs. Connecting AI to core systems, data sources and legacy applications. Tool calling and the Model Context Protocol (MCP). AI gateways. Latency, reliability and error handling.

**Module 10. Generative AI Architecture Patterns**  
A synthesis of the patterns seen so far: prompt-based, RAG, workflow, agentic and fine-tuning. Comparing patterns by cost, complexity and risk, and choosing the right one for a use case.

### Afternoon

**Module 11. AI Security, Privacy and Responsible AI**  
The threat landscape: direct and indirect prompt injection, data leakage, jailbreaks, data and model poisoning, with reference to OWASP guidance. Privacy by design and protection of personal data. Fairness, transparency and explainability.

> **Demo 4 — Attacking the policy assistant**  
> Python notebook. The Demo 2 assistant is attacked through a poisoned document (indirect prompt injection) and a personal data leakage scenario. Mitigations are applied and compared.

**Module 12. AI Governance and Compliance**  
The EU AI Act and its risk classification, including high-risk uses such as creditworthiness assessment. GDPR. DORA and third-party ICT risk. Model risk management. Roles, policies and documentation.

**Module 13. MLOps and LLMOps Fundamentals**  
The lifecycle of ML and LLM systems. Versioning of models, prompts and data. Continuous evaluation. Deployment and release strategies.

**Module 14. Building AI Applications on Cloud Platforms (GCP, Azure, AWS)**  
A reference architecture on Microsoft Azure and its main AI services. Equivalent services on Google Cloud and AWS. Build versus buy.

**Module 15. Monitoring, Observability and Cost Management for AI Workloads**  
What to monitor: quality, drift, latency, errors and usage. Tracing LLM and agent calls. The token-based cost model and optimisation techniques (caching, model routing, prompt size).
