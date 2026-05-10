# Awesome Code as Agent Harness Papers

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
[![arXiv](https://img.shields.io/badge/arXiv-XXXX.XXXXX-b31b1b.svg)](#)  <!-- TODO: replace with real arXiv link once posted -->
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Contributions Welcome](https://img.shields.io/badge/Contributions-Welcome-brightgreen.svg)](#-contributing)
![Last Commit](https://img.shields.io/github/last-commit/YennNing/Awesome-Code-as-Agent-Harness-Papers)
![Visitors](https://visitor-badge.laobi.icu/badge?page_id=YennNing.Awesome-Code-as-Agent-Harness-Papers)

This repository organizes research that treats **code and its execution artifacts as the executable, inspectable, and stateful infrastructure** through which LLM agents reason, act, model environments, manage state, and verify progress. Papers are grouped along three connected layers — *Harness Interface*, *Harness Mechanisms*, and *Scaling the Harness* — and across applications such as coding assistants, GUI/OS automation, scientific discovery, embodied agents, and recommender systems.

> 📄 **Based on the survey**: *Code as Agent Harness: Toward Executable, Verifiable, and Stateful Agent Systems* (arXiv link coming soon — placeholder)

![Framework overview](figs/overview.png)

## 🔔 News

**[TBD]** 🚀 We will release a comprehensive survey on ***Code as Agent Harness***. The arXiv preprint, slides, and project page links will be added here once available.

## 📋 Table of Contents

- [🔔 News](#-news)
- [📋 Table of Contents](#-table-of-contents)
- [🌟 Introduction](#-introduction)
- [🤝 Contributing](#-contributing)
- [📝 Citation](#-citation)
- [🧩 Harness Interface](#-harness-interface)
  - [💭 Code for Reasoning](#-code-for-reasoning)
  - [🤖 Code for Acting](#-code-for-acting)
  - [🌍 Code for Environment Modeling](#-code-for-environment-modeling)
- [🛠️ Harness Mechanisms](#%EF%B8%8F-harness-mechanisms)
  - [🗺️ Planning for Code Agents](#%EF%B8%8F-planning-for-code-agents)
  - [🧠 Memory and Context Engineering](#-memory-and-context-engineering)
  - [🔧 Tool Usage for Code Agents](#-tool-usage-for-code-agents)
  - [🧪 Feedback-Guided Iterative Debugging](#-feedback-guided-iterative-debugging)
- [👥 Scaling the Harness: Multi-Agent Code-Centric Systems](#-scaling-the-harness-multi-agent-code-centric-systems)
  - [🎭 Functional Role Specialization](#-functional-role-specialization)
  - [💬 Interaction Modes](#-interaction-modes)
  - [🕸️ Workflow Topology](#%EF%B8%8F-workflow-topology)
  - [⚡ Execution Feedback Integration](#-execution-feedback-integration)
  - [🔄 Shared-Harness Synchronization](#-shared-harness-synchronization)
  - [🏛️ Shared Harness Representation](#%EF%B8%8F-shared-harness-representation)
  - [🎯 Harness-State Convergence](#-harness-state-convergence)
- [🚀 Applications and Emerging Fields](#-applications-and-emerging-fields)
  - [💻 Code Assistants](#-code-assistants)
  - [🖥️ GUI / OS Agents](#%EF%B8%8F-gui--os-agents)
  - [🔬 Scientific Discovery Agents](#-scientific-discovery-agents)
  - [🤖 Autonomous Embodied Agents](#-autonomous-embodied-agents)
  - [🎬 Agent Personalization (Recommender Systems)](#-agent-personalization-recommender-systems)

---

## 🌟 Introduction

Recent large language models (LLMs) have demonstrated strong capabilities in understanding and generating code, but their role in agentic systems is shifting from *target output* to *operational substrate*. We introduce **Code as Agent Harness**: code and its execution artifacts (programs, traces, repositories, tests, sandboxes, simulators) are the executable, inspectable, and stateful infrastructure through which LLM agents operate reliably over time.

We organize the literature into three connected layers:

🔹 **Harness Interface.** How code enters the agent loop — externalizing reasoning into executable procedures, translating intent into programmable actions, and modeling environment state through program artifacts, traces, and simulations.

🔹 **Harness Mechanisms.** How a code-harnessed agent stays reliable over long horizons — planning organizes the trajectory, memory preserves task state, tool use connects to external systems, and iterative debugging turns execution failures into revision signals.

🔹 **Scaling the Harness.** How code becomes a shared workspace for multi-agent systems — coordinating roles, exchanging artifacts, reviewing each other’s outputs, and verifying collective progress through repositories, execution states, and structured workflows.

Across these layers, we synthesize methodological progress and practical applications in coding assistants, GUI/OS automation, embodied agents, scientific discovery, recommender systems, DevOps, and enterprise workflows.

## 🤝 Contributing

This collection is an ongoing effort. We welcome contributions from the community:

- Submit a pull request to add papers or resources
- Open an issue to suggest additional papers
- Email us at: *(placeholder — corresponding-author email goes here)*

We regularly update the repository to include new research on code-centric agentic systems.

## 📝 Citation

If you find this repository or paper useful, please consider citing the survey:

```bibtex
@article{ning2026codeasharness,
  title   = {Code as Agent Harness: Toward Executable, Verifiable, and Stateful Agent Systems},
  author  = {Ning, Xuying and Tieu, Katherine and Fu, Dongqi and Wei, Tianxin and Li, Zihao and Bei, Yuanchen and others},
  journal = {arXiv preprint arXiv:XXXX.XXXXX},  % TODO: replace once posted
  year    = {2026}
}
```

---

## 🧩 Harness Interface

Code as the basic interface between a model and its task environment. Programs convert model outputs into executable, inspectable, and stateful structures: code makes reasoning *executable*, action *programmable*, and environment state *inspectable*.

### 💭 Code for Reasoning

Programs externalize internal logic into verifiable computation, allowing interpreters, symbolic solvers, execution traces, or process rewards to check and refine intermediate steps.

#### Program-Delegated Reasoning

| Paper | Venue |
| --- | --- |
| [Program of thoughts prompting: Disentangling computation from reasoning for numerical reasoning tasks](https://arxiv.org/abs/2211.12588) | TMLR 2022 |
| [Mathcoder: Seamless code integration in llms for enhanced mathematical reasoning](https://arxiv.org/abs/2310.03731) | ICLR 2023 |
| [Chain of code: Reasoning with a language model-augmented code emulator](https://arxiv.org/abs/2312.04474) | ICML 2023 |
| [Method-based reasoning for large language models: Extraction, reuse, and continuous improvement](https://arxiv.org/abs/2508.04289) | 2025 |
| [Code-enabled language models can outperform reasoning models on diverse tasks](https://arxiv.org/abs/2510.20909) | 2025 |

#### Hybrid Symbolic–Neural Execution

| Paper | Venue |
| --- | --- |
| [Self-Verifying Reflection Helps Transformers with CoT Reasoning](https://arxiv.org/abs/2510.12157) | 2025 |
| [SSR: Socratic Self-Refine for Large Language Model Reasoning](https://arxiv.org/abs/2511.10621) | 2025 |
| [CodeSteer: Symbolic-Augmented Language Models via Code/Text Guidance](https://arxiv.org/abs/2502.04350) | ICML 2025 |

#### Iterative Code-Grounded Reasoning

| Paper | Venue |
| --- | --- |
| [Next: Teaching large language models to reason about code execution](https://arxiv.org/abs/2404.14662) | ICML 2024 |
| [What I cannot execute, I do not understand: Training and Evaluating LLMs on Program Execution Traces](https://arxiv.org/abs/2503.05703) | 2025 |
| [Reasoning through execution: Unifying process and outcome rewards for code generation](https://arxiv.org/abs/2412.15118) | ICML 2024 |
| [CodeRL+: Improving Code Generation via Reinforcement with Execution Semantics Alignment](https://arxiv.org/abs/2510.18471) | 2025 |
| [Rltf: Reinforcement learning from unit test feedback](https://arxiv.org/abs/2307.04349) | TMLR 2023 |
| [Rlef: Grounding code llms in execution feedback with reinforcement learning](https://arxiv.org/abs/2410.02089) | ICML 2024 |
| [Execution guided line-by-line code generation](https://arxiv.org/abs/2506.10948) | 2025 |

### 🤖 Code for Acting

Generated programs serve as policies, tool calls, behavior trees, or reusable skills for embodied, GUI, software, and tool-use environments.

#### Grounded Skill Selection

| Paper | Venue |
| --- | --- |
| [Do as i can, not as i say: Grounding language in robotic affordances](https://arxiv.org/abs/2204.01691) | CoRL 2022 |
| [Robots that ask for help: Uncertainty alignment for large language model planners](https://arxiv.org/abs/2307.01928) | CoRL 2023 |
| [Bootstrap your own skills: Learning to solve new tasks with large language model guidance](https://arxiv.org/abs/2310.10021) | CoRL 2023 |
| [SkillVLA: Tackling Combinatorial Diversity in Dual-Arm Manipulation via Skill Reuse](https://arxiv.org/abs/2603.03836) | 2026 |

#### Programmatic Policy Generation

| Paper | Venue |
| --- | --- |
| [Robocodex: Multimodal code generation for robotic behavior synthesis](https://arxiv.org/abs/2402.16117) | ICML 2024 |
| [Cp-agent: Agentic constraint programming](https://arxiv.org/abs/2508.07468) | 2025 |
| [LLM-Driven Corrective Robot Operation Code Generation with Static Text-Based Simulation](https://arxiv.org/abs/2512.02002) | 2025 |
| [NormCode: A Semi-Formal Language for Auditable AI Planning](https://arxiv.org/abs/2512.10563) | 2025 |
| [ALRM: Agentic LLM for Robotic Manipulation](https://arxiv.org/abs/2601.19510) | 2026 |
| [RACAS: Controlling Diverse Robots With a Single Agentic System](https://arxiv.org/abs/2603.05621) | 2026 |
| [ReAct: Synergizing Reasoning and Acting in Language Models](https://arxiv.org/abs/2210.03629) | 2023 ❓ |

#### Lifelong Code-Based Agents

| Paper | Venue |
| --- | --- |
| [Growing with your embodied agent: A human-in-the-loop lifelong code generation framework for long-horizon manipulation skills](https://arxiv.org/abs/2509.18597) | 2025 |
| [Vireskill: Vision-grounded replanning with skill memory for llm-based planning in lifelong robot learning](https://arxiv.org/abs/2509.24219) | 2025 |
| [UI-Voyager: A Self-Evolving GUI Agent Learning via Failed Experience](https://arxiv.org/abs/2603.24533) | 2026 |

### 🌍 Code for Environment Modeling

Program states, repositories, traces, simulators, and tests represent state, dynamics, and feedback signals for agent interaction.

#### Structured World Representations

| Paper | Venue |
| --- | --- |
| [From Programs to Poses: Factored Real-World Scene Generation via Learned Program Libraries](https://arxiv.org/abs/2510.10292) | 2025 |
| [Poe-world: Compositional world modeling with products of programmatic experts](https://arxiv.org/abs/2505.10819) | 2025 |
| [Code2world: A gui world model via renderable code generation](https://arxiv.org/abs/2602.09856) | 2026 |
| [Code2Worlds: Empowering Coding LLMs for 4D World Generation](https://arxiv.org/abs/2602.11757) | 2026 |

#### Execution-Trace World Modeling

| Paper | Venue |
| --- | --- |
| [Semcoder: Training code language models with comprehensive semantics](https://arxiv.org/abs/2406.01006) | NeurIPS 2024 |
| [Cwm: An open-weights llm for research on code generation with world models](https://arxiv.org/abs/2510.02387) | 2025 |
| [Reinforcement World Model Learning for LLM-based Agents](https://arxiv.org/abs/2602.05842) | 2026 |
| [Agent world model: Infinity synthetic environments for agentic reinforcement learning](https://arxiv.org/abs/2602.10090) | 2026 |
| [Aligning Agentic World Models via Knowledgeable Experience Learning](https://arxiv.org/abs/2601.13247) | 2026 |

#### Code-Grounded Evaluation Environments

| Paper | Venue |
| --- | --- |
| [Cruxeval: A benchmark for code reasoning, understanding and execution](https://arxiv.org/abs/2401.03065) | ICML 2024 |
| [Livecodebench: Holistic and contamination free evaluation of large language models for code](https://arxiv.org/abs/2403.07974) | ICLR 2024 |
| [Swe-bench: Can language models resolve real-world github issues?](https://arxiv.org/abs/2310.06770) | ICLR 2023 |
| [Agentbench: Evaluating llms as agents](https://arxiv.org/abs/2308.03688) | ICLR 2023 |
| [Core: Benchmarking llms code reasoning capabilities through static analysis tasks](https://arxiv.org/abs/2507.05269) | 2025 |
| [Geogrambench: Benchmarking the geometric program reasoning in modern llms](https://arxiv.org/abs/2505.17653) | 2025 |
| [CodeGlance: Understanding Code Reasoning Challenges in LLMs through Multi-Dimensional Feature Analysis](https://arxiv.org/abs/2602.13962) | 2026 |
| [Endless Terminals: Scaling RL Environments for Terminal Agents](https://arxiv.org/abs/2601.16443) | 2026 |

## 🛠️ Harness Mechanisms

Once code is placed inside the agent loop, the harness must decide *what to execute next*, *preserve useful state*, *expose the right tools*, and *convert failures into corrective actions*.

### 🗺️ Planning for Code Agents

Planning is harness control: it structures how the agent externalizes intent into executable steps, schedules interactions with code artifacts and tools, and regulates the trajectory of reasoning, execution, and revision over time.

#### Linear Decomposition Planning

| Paper | Venue |
| --- | --- |
| [A real-world webagent with planning, long context understanding, and program synthesis](https://arxiv.org/abs/2307.12856) | ICLR 2023 |
| [ReAct: Synergizing Reasoning and Acting in Language Models](https://arxiv.org/abs/2210.03629) | 2023 ❓ |

#### Structure-Grounded Planning

| Paper | Venue |
| --- | --- |
| [RPG: A Repository Planning Graph for Unified and Scalable Codebase Generation](https://arxiv.org/abs/2509.16198) | 2025 |
| [Code graph model (cgm): A graph-integrated large language model for repository-level software engineering tasks](https://arxiv.org/abs/2505.16901) | 2025 |
| [DomAgent: Leveraging Knowledge Graphs and Case-Based Reasoning for Domain-Specific Code Generation](https://arxiv.org/abs/2603.21430) | 2026 |

#### Search-Based Planning

| Paper | Venue |
| --- | --- |
| [Planning in natural language improves llm search for code generation](https://arxiv.org/abs/2409.03733) | ICLR 2025 |
| [Tree-of-code: A tree-structured exploring framework for end-to-end code generation and execution in complex task handling](https://arxiv.org/abs/2412.15305) | ACL 2025 Findings |
| [Let's Revise Step-by-Step: A Unified Local Search Framework for Code Generation with LLMs](https://arxiv.org/abs/2508.07434) | 2025 |
| [Meta-Harness: End-to-End Optimization of Model Harnesses](https://arxiv.org/abs/2603.28052) | 2026 |

#### Orchestration-Based Planning

| Paper | Venue |
| --- | --- |
| [Agentcoder: Multi-agent-based code generation with iterative testing and optimisation](https://arxiv.org/abs/2312.13010) | 2023 |
| [AutoSafeCoder: A multi-agent framework for securing LLM code generation through static analysis and fuzz testing](https://arxiv.org/abs/2402.04486) | 2024 |
| [CodeCoR: An LLM-based self-reflective multi-agent framework for code generation](https://arxiv.org/abs/2501.05678) | 2025 |
| [Multi-Agent Code-Orchestrated Generation for Reliable Infrastructure-as-Code](https://arxiv.org/abs/2510.03902) | 2025 |
| [SGAgent: Suggestion-Guided LLM-Based Multi-Agent Framework for Repository-Level Software Repair](https://arxiv.org/abs/2602.23647) | 2026 |
| [Requirements Development and Formalization for Reliable Code Generation: A Multi-Agent Vision](https://arxiv.org/abs/2508.18675) | ASE 2025 |

### 🧠 Memory and Context Engineering

Memory in code-as-agent-harness systems is a state-management layer: which information stays in the active context, which is compacted, and which is offloaded to durable external storage.

#### Working Memory

| Paper | Venue |
| --- | --- |
| [Language Models Do Not Have Human-Like Working Memory](https://arxiv.org/abs/2505.10571) | 2025 |
| [Live-SWE-agent: Can Software Engineering Agents Self-Evolve on the Fly?](https://arxiv.org/abs/2511.13646) | 2025 |
| [CodeMem: Architecting Reproducible Agents via Dynamic MCP and Procedural Memory](https://arxiv.org/abs/2512.15813) | 2025 |

#### Semantic Memory

| Paper | Venue |
| --- | --- |
| [From human memory to ai memory: A survey on memory mechanisms in the era of llms](https://arxiv.org/abs/2504.15965) | 2025 |
| [Rethinking Memory Mechanisms of Foundation Agents in the Second Half](https://arxiv.org/abs/2602.06052) | 2026 |
| [AgentSM: Semantic Memory for Agentic Text-to-SQL](https://arxiv.org/abs/2601.15709) | 2026 |

#### Experiential Memory

| Paper | Venue |
| --- | --- |
| [Evo-memory: Benchmarking llm agent test-time learning with self-evolving memory](https://arxiv.org/abs/2511.20857) | 2025 |
| [MemGovern: Enhancing Code Agents through Learning from Governed Human Experiences](https://arxiv.org/abs/2601.06789) | 2026 |
| [Leveraging prior experience: An expandable auxiliary knowledge base for text-to-sql](https://arxiv.org/abs/2411.13244) | 2024 |

#### Long-Term Memory

| Paper | Venue |
| --- | --- |
| [Memex (RL): Scaling Long-Horizon LLM Agents via Indexed Experience Memory](https://arxiv.org/abs/2603.04257) | 2026 |
| [Mem-gallery: Benchmarking multimodal long-term conversational memory for mllm agents](https://arxiv.org/abs/2601.03515) | 2026 |
| [MemGPT: Towards LLMs as Operating Systems](https://arxiv.org/abs/2310.08560) | 2023 |
| [Your Code Agent Can Grow Alongside You with Structured Memory](https://arxiv.org/abs/2603.13258) | 2026 |
| [TALM: Dynamic Tree-Structured Multi-Agent Framework with Long-Term Memory for Scalable Code Generation](https://arxiv.org/abs/2510.23010) | 2025 |

#### Multi-Agent Memory

| Paper | Venue |
| --- | --- |
| [Swe-debate: Competitive multi-agent debate for software issue resolution](https://arxiv.org/abs/2507.23348) | 2025 |
| [Gamegpt: Multi-agent collaborative framework for game development](https://arxiv.org/abs/2310.08067) | 2023 |
| [Agentcoder: Multi-agent-based code generation with iterative testing and optimisation](https://arxiv.org/abs/2312.13010) | 2023 |
| [Mirix: Multi-agent memory system for llm-based agents](https://arxiv.org/abs/2507.07957) | 2025 |
| [Self-organized agents: A LLM multi-agent framework toward ultra large-scale code generation and optimization](https://arxiv.org/abs/2404.02183) | 2024 |
| [Compressing Code Context for LLM-based Issue Resolution](https://arxiv.org/abs/2603.28119) | 2026 |
| [Scaling long-horizon llm agent via context-folding](https://arxiv.org/abs/2510.11967) | 2025 |
| [LongCLI-Bench: A Preliminary Benchmark and Study for Long-horizon Agentic Programming in Command-Line Interfaces](https://arxiv.org/abs/2602.14337) | 2026 |

### 🔧 Tool Usage for Code Agents

Tool usage is the action and observation layer of the code-agent harness: agents search repositories, inspect files, edit code, run commands, execute tests, call APIs, and verify intermediate results — all under typed schemas, sandboxes, and lifecycle hooks.

#### Function-Oriented Tool Use

| Paper | Venue |
| --- | --- |
| [Toolcoder: Teach code generation models to use api search tools](https://arxiv.org/abs/2305.04032) | 2023 |

#### Environment-Interaction Tool Use

| Paper | Venue |
| --- | --- |
| [Environment-in-the-Loop: Rethinking Code Migration with LLM-based Agents](https://arxiv.org/abs/2602.09944) | 2026 |

#### Verification-Driven Tool Use

| Paper | Venue |
| --- | --- |
| [Veriguard: Enhancing llm agent safety via verified code generation](https://arxiv.org/abs/2510.05156) | 2025 |
| [Agentcoder: Multi-agent-based code generation with iterative testing and optimisation](https://arxiv.org/abs/2312.13010) | 2023 |

#### Workflow-Orchestration Tool Use

| Paper | Venue |
| --- | --- |
| [Toolnet: Connecting large language models with massive tools via tool graph](https://arxiv.org/abs/2403.00839) | 2024 |

### 🧪 Feedback-Guided Iterative Debugging

Iterative debugging closes the harness loop: development environments expose feedback (compiler diagnostics, runtime errors, tests, critique), and the agent transforms these signals into diagnosis, revision, and progressively better debugging behavior.

#### Development Environments for Agentic Coding

##### Contextual Environments for Repository-Aware Generation

| Paper | Venue |
| --- | --- |
| [On the Impacts of Contexts on Repository-Level Code Generation](https://aclanthology.org/2025.findings-naacl.82/) | NAACL 2025 Findings |
| [A Survey on Model Context Protocol: Architecture, State-of-the-art, Challenges and Future Directions](https://api.semanticscholar.org/CorpusID:281419186) |  arXiv|
| [CodexGraph: Bridging Large Language Models and Code Repositories via Code Graph Databases](https://arxiv.org/abs/2408.03910) | NAACL 2024 |
| [RepoAgent: An LLM-Powered Open-Source Framework for Repository-level Code Documentation Generation](https://aclanthology.org/2024.emnlp-demo.46/) | EMNLP 2024 Demo |
| [Knowledge Graph Based Repository-Level Code Generation](http://dx.doi.org/10.1109/LLM4Code66737.2025.00026) | Workshop 2025 |
| [From glue-code to protocols: A critical analysis of a2a and mcp integration for scalable agent systems](https://arxiv.org/abs/2505.03864) | 2025 |
| [Retrieval-Augmented Code Generation: A Survey with Focus on Repository-Level Approaches](https://arxiv.org/abs/2510.04905) | 2026 |

##### Interactive Environments for Human–LLM Collaboration

| Paper | Venue |
| --- | --- |
| [Conversational AI as a Coding Assistant: Understanding Programmers' Interactions with and Expectations from Large Language Models for Coding](https://arxiv.org/abs/2503.16508) | 2025 |
| [The Design Space of LLM-Based AI Coding Assistants: An Analysis of 90 Systems in Academia and Industry](https://api.semanticscholar.org/CorpusID:282143017) | IEEE Symposium on Visual Languages / Human-Centric Computing Languages and Environments 2025 |
| [language-server-protocol: Defines a common protocol for language servers](https://github.com/Microsoft/language-server-protocol) | Web/Blog |
| [Deductive verification via the debug adapter protocol](https://arxiv.org/abs/2108.02968) | F-IDE@NFM 2021 |

##### Execution and Validation Environments

| Paper | Venue |
| --- | --- |
| [RepoST: Scalable Repository-Level Coding Environment Construction with Sandbox Testing](https://arxiv.org/abs/2503.07358) | 2025 |
| [Klear-CodeTest: Scalable Test Case Generation for Code Reinforcement Learning](https://arxiv.org/abs/2508.05710) | 2025 |
| [FeedbackEval: A Benchmark for Evaluating Large Language Models in Feedback-Driven Code Repair Tasks](https://arxiv.org/abs/2504.06939) | 2026 |
| [LLMLOOP: Improving LLM-Generated Code and Tests Through Automated Iterative Feedback Loops](https://doi.org/10.1109/ICSME64153.2025.00109) | IEEE International Conference on Software Maintenance and Evolution 2025 |
| [Openagentsafety: A comprehensive framework for evaluating real-world ai agent safety](https://arxiv.org/abs/2507.06134) | 2025 |
| [Kubeintellect: A modular llm-orchestrated agent framework for end-to-end kubernetes management](https://arxiv.org/abs/2509.02449) | 2025 |

##### Engineering Platforms for Deployment and Workflow Integration

| Paper | Venue |
| --- | --- |
| [LLM-Based Multi-Agent Systems for Software Engineering: Literature Review, Vision, and the Road Ahead](https://doi.org/10.1145/3712003) | TOSEM 2024 |
| [AgentMesh: A Cooperative Multi-Agent Generative AI Framework for Software Development Automation](https://arxiv.org/abs/2507.19902) | 2025 |
| [ALMAS: an Autonomous LLM-based Multi-Agent Software Engineering Framework](https://arxiv.org/abs/2510.03463) | Workshop @ ASE 2025 |
| [From challenges to metrics: An LLM-driven DevOps recommendation system grounded in evidence-based mappings](https://www.sciencedirect.com/science/article/pii/S2590005625001742) | Array 2025 |
| [AI Augmented CI/CD Pipelines: From Code Commit to Production with Autonomous Decisions](http://dx.doi.org/10.1109/FLLM67465.2025.11391007) | 2025 3rd International Conference on Foundation and Large Language Models (FLLM) 2025 |
| [A Multi-Agent Coding Assistant for Cloud-Native Development: From Requirements to Deployable Microservices](https://doi.org/10.20944/preprints202512.1922.v1) | Science 2025 |

#### Feedback Mechanisms for Iterative Debugging

##### Compilation and Static-Analysis Feedback

| Paper | Venue |
| --- | --- |
| [The Debugging Decay Index: Rethinking Debugging Strategies for Code LLMs](https://arxiv.org/abs/2506.18403) | 2025 |
| [Helping llms improve code generation using feedback from testing and static analysis](https://arxiv.org/abs/2412.14841) | Discover Artificial Intelligence 2024 |
| [Enhancing llm code generation: A systematic evaluation of multi-agent collaboration and runtime debugging for improved accuracy, reliability, and latency](https://arxiv.org/abs/2505.02133) | 2025 |

##### Runtime Error and Exception Feedback

| Paper | Venue |
| --- | --- |
| [Llm as runtime error handler: A promising pathway to adaptive self-healing of software systems](https://arxiv.org/abs/2408.01055) | 2024 |
| [Large language model guided self-debugging code generation](https://arxiv.org/abs/2502.02928) | 2025 |

##### Test-Based Execution Feedback

| Paper | Venue |
| --- | --- |
| [Teaching large language models to self-debug](https://arxiv.org/abs/2304.05128) | ICLR 2023 |
| [Learning to generate unit tests for automated debugging](https://arxiv.org/abs/2502.01619) | 2025 |
| [Testart: Improving llm-based unit testing via co-evolution of automated generation and repair iteration](https://arxiv.org/abs/2408.03095) | 2024 |
| [From Code to Correctness: Closing the Last Mile of Code Generation with Hierarchical Debugging](https://openreview.net/forum?id=dwQIVcW1du) | 2025 |

##### Critique-Driven Feedback (Human or Auxiliary Agents)

| Paper | Venue |
| --- | --- |
| [Interactive Debugging and Steering of Multi-Agent AI Systems](https://doi.org/10.1145/3706598.3713581) | CHI 2025 |
| [RGD: Multi-LLM Based Agent Debugger via Refinement and Generation Guidance](https://doi.org/10.1109/ICA63002.2024.00037) | International Conference on Agents 2024 |

##### Feedback-Driven Debugging and Self-Improvement

| Paper | Venue |
| --- | --- |
| [IterPref: Focal Preference Learning for Code Generation via Iterative Debugging](https://api.semanticscholar.org/CorpusID:282402257) | 2025 |
| [ReVeal: Self-Evolving Code Agents via Reliable Self-Verification](https://arxiv.org/abs/2506.11442) | 2025 |

## 👥 Scaling the Harness: Multi-Agent Code-Centric Systems

When multiple agents operate over code, the harness must coordinate roles, share intermediate artifacts, maintain common state, and verify collective progress through repositories, tests, traces, and structured workflows.

### 🎭 Functional Role Specialization

Distinct agents own slices of the shared code harness — synthesis, understanding, verification, execution, and planning.

#### Program Synthesis Agents

| Paper | Venue |
| --- | --- |
| [Agentcoder: Multi-agent-based code generation with iterative testing and optimisation](https://arxiv.org/abs/2312.13010) | 2023 |
| [MetaGPT: Meta Programming for A Multi-Agent Collaborative Framework](https://openreview.net/forum?id=VtmBAGCN7o) | ICLR 2024 |
| [ChatDev: Communicative Agents for Software Development](https://doi.org/10.18653/v1/2024.acl-long.810) | ACL 2024 |
| [MAGE: A multi-agent engine for automated RTL code generation](https://arxiv.org/abs/2406.03554) | DAC 2025 |

#### Program Understanding Agents

| Paper | Venue |
| --- | --- |
| [HyperAgent: Generalist software engineering agents to solve coding tasks at scale](https://arxiv.org/abs/2406.11915) | 2024 |
| [Lingma SWE-GPT: An Open Development-Process-Centric Language Model for Automated Software Improvement](https://doi.org/10.48550/arXiv.2411.00622) | 2024 |
| [CleanAgent: Automating data standardization with LLM-based agents](https://arxiv.org/abs/2403.08291) | 2024 |

#### Verification Agents

| Paper | Venue |
| --- | --- |
| [QualityFlow: An agentic workflow for program synthesis controlled by LLM quality checks](https://arxiv.org/abs/2501.01234) | 2025 |
| [AutoSafeCoder: A multi-agent framework for securing LLM code generation through static analysis and fuzz testing](https://arxiv.org/abs/2402.04486) | 2024 |
| [Hallucination to consensus: Multi-agent LLMs for end-to-end test generation with accurate oracles](https://arxiv.org/abs/2501.11223) | 2025 |

#### Execution Agents

*(No papers with available URL.)*

#### Planning Agents

| Paper | Venue |
| --- | --- |
| [Self-organized agents: A LLM multi-agent framework toward ultra large-scale code generation and optimization](https://arxiv.org/abs/2404.02183) | 2024 |

### 💬 Interaction Modes

Code-centric multi-agent interaction is artifact-mediated: agents observe and modify shared code, and grounding comes from the objective state exposed by execution.

#### Collaborative Synthesis

| Paper | Venue |
| --- | --- |
| [Codepori: Large-scale system for autonomous software development using multi-agent technology](https://arxiv.org/abs/2405.10931) | 2024 |

#### Critique and Repair

| Paper | Venue |
| --- | --- |
| [Agentcoder: Multi-agent-based code generation with iterative testing and optimisation](https://arxiv.org/abs/2312.13010) | 2023 |
| [SEW: Self-evolving agentic workflows for automated code generation](https://arxiv.org/abs/2502.01234) | 2025 |

#### Adversarial Validation

| Paper | Venue |
| --- | --- |
| [AutoSafeCoder: A multi-agent framework for securing LLM code generation through static analysis and fuzz testing](https://arxiv.org/abs/2402.04486) | 2024 |
| [MAGE: A multi-agent engine for automated RTL code generation](https://arxiv.org/abs/2406.03554) | DAC 2025 |

#### Reasoning Debate

| Paper | Venue |
| --- | --- |
| [ChatDev: Communicative Agents for Software Development](https://doi.org/10.18653/v1/2024.acl-long.810) | ACL 2024 |
| [Hallucination to consensus: Multi-agent LLMs for end-to-end test generation with accurate oracles](https://arxiv.org/abs/2501.11223) | 2025 |

### 🕸️ Workflow Topology

Topology of agent interaction (chain, cyclic, hierarchical, star, adaptive) is one of the most consequential design decisions in multi-agent code generation.

#### Pre-Defined Heuristic Topologies (Waterfall / Iterative / Hierarchical / Star)

| Paper | Venue |
| --- | --- |
| [ChatDev: Communicative Agents for Software Development](https://doi.org/10.18653/v1/2024.acl-long.810) | ACL 2024 |
| [MetaGPT: Meta Programming for A Multi-Agent Collaborative Framework](https://openreview.net/forum?id=VtmBAGCN7o) | ICLR 2024 |
| [L2MAC: Large language model automatic computer for extensive code generation](https://arxiv.org/abs/2310.02003) | ICLR 2024 |
| [Agentcoder: Multi-agent-based code generation with iterative testing and optimisation](https://arxiv.org/abs/2312.13010) | 2023 |
| [MAGE: A multi-agent engine for automated RTL code generation](https://arxiv.org/abs/2406.03554) | DAC 2025 |
| [HyperAgent: Generalist software engineering agents to solve coding tasks at scale](https://arxiv.org/abs/2406.11915) | 2024 |
| [Self-organized agents: A LLM multi-agent framework toward ultra large-scale code generation and optimization](https://arxiv.org/abs/2404.02183) | 2024 |
| [Hallucination to consensus: Multi-agent LLMs for end-to-end test generation with accurate oracles](https://arxiv.org/abs/2501.11223) | 2025 |

#### Objective-Driven and Adaptive Topologies

| Paper | Venue |
| --- | --- |
| [FlowReasoner: Reinforcing Query-Level Meta-Agents](https://arxiv.org/abs/2504.15257) | 2025 |
| [BOAD: Discovering Hierarchical Software Engineering Agents via Bandit Optimization](https://arxiv.org/abs/2512.23631) | 2025 |
| [SEW: Self-evolving agentic workflows for automated code generation](https://arxiv.org/abs/2502.01234) | 2025 |

### ⚡ Execution Feedback Integration

Code is uniquely executable, producing objective oracle signals that anchor multi-agent coordination.

#### Compiler and Syntax Feedback

| Paper | Venue |
| --- | --- |
| [ChatDev: Communicative Agents for Software Development](https://doi.org/10.18653/v1/2024.acl-long.810) | ACL 2024 |
| [L2MAC: Large language model automatic computer for extensive code generation](https://arxiv.org/abs/2310.02003) | ICLR 2024 |

#### Test Pass/Fail Signals

| Paper | Venue |
| --- | --- |
| [Agentcoder: Multi-agent-based code generation with iterative testing and optimisation](https://arxiv.org/abs/2312.13010) | 2023 |
| [QualityFlow: An agentic workflow for program synthesis controlled by LLM quality checks](https://arxiv.org/abs/2501.01234) | 2025 |

#### Fuzzer Crash Traces

| Paper | Venue |
| --- | --- |
| [AutoSafeCoder: A multi-agent framework for securing LLM code generation through static analysis and fuzz testing](https://arxiv.org/abs/2402.04486) | 2024 |

#### Static Analysis Warnings

*(No papers with available URL.)*

#### Performance Profiling Results

| Paper | Venue |
| --- | --- |
| [MARCO: Multi-Agent Code Optimization with Real-Time Knowledge Integration for High-Performance Computing](https://arxiv.org/abs/2505.03906) | 2025 |

#### Fine-Grained Simulation Feedback

| Paper | Venue |
| --- | --- |
| [MAGE: A multi-agent engine for automated RTL code generation](https://arxiv.org/abs/2406.03554) | DAC 2025 |

### 🔄 Shared-Harness Synchronization

How multi-agent systems maintain a consistent shared view of program state.

#### Shared Blackboard

| Paper | Venue |
| --- | --- |
| [L2MAC: Large language model automatic computer for extensive code generation](https://arxiv.org/abs/2310.02003) | ICLR 2024 |

#### Parallel Branches with Merge

| Paper | Venue |
| --- | --- |
| [HyperAgent: Generalist software engineering agents to solve coding tasks at scale](https://arxiv.org/abs/2406.11915) | 2024 |

#### Structured Context Scheduling

| Paper | Venue |
| --- | --- |
| [MetaGPT: Meta Programming for A Multi-Agent Collaborative Framework](https://openreview.net/forum?id=VtmBAGCN7o) | ICLR 2024 |

#### Hierarchical Memory

| Paper | Venue |
| --- | --- |
| [ChatDev: Communicative Agents for Software Development](https://doi.org/10.18653/v1/2024.acl-long.810) | ACL 2024 |
| [Cogito, ergo sum: A neurobiologically-inspired cognition-memory-growth system for code generation](https://arxiv.org/abs/2501.03456) | 2025 |

#### Agent Pool Scaling

| Paper | Venue |
| --- | --- |
| [Self-organized agents: A LLM multi-agent framework toward ultra large-scale code generation and optimization](https://arxiv.org/abs/2404.02183) | 2024 |

### 🏛️ Shared Harness Representation

Four levels of formalization for the shared substrate: implicit/file-only, repository-based, execution-based, and blackboard.

#### Implicit / File-Only Representation

| Paper | Venue |
| --- | --- |
| [ChatDev: Communicative Agents for Software Development](https://doi.org/10.18653/v1/2024.acl-long.810) | ACL 2024 |
| [MetaGPT: Meta Programming for A Multi-Agent Collaborative Framework](https://openreview.net/forum?id=VtmBAGCN7o) | ICLR 2024 |
| [CodeCoR: An LLM-based self-reflective multi-agent framework for code generation](https://arxiv.org/abs/2501.05678) | 2025 |
| [SEW: Self-evolving agentic workflows for automated code generation](https://arxiv.org/abs/2502.01234) | 2025 |
| [Codepori: Large-scale system for autonomous software development using multi-agent technology](https://arxiv.org/abs/2405.10931) | 2024 |

#### Repository-Based Representation

| Paper | Venue |
| --- | --- |
| [HyperAgent: Generalist software engineering agents to solve coding tasks at scale](https://arxiv.org/abs/2406.11915) | 2024 |
| [Lingma SWE-GPT: An Open Development-Process-Centric Language Model for Automated Software Improvement](https://doi.org/10.48550/arXiv.2411.00622) | 2024 |

#### Execution-Based Representation

| Paper | Venue |
| --- | --- |
| [Agentcoder: Multi-agent-based code generation with iterative testing and optimisation](https://arxiv.org/abs/2312.13010) | 2023 |
| [AutoSafeCoder: A multi-agent framework for securing LLM code generation through static analysis and fuzz testing](https://arxiv.org/abs/2402.04486) | 2024 |
| [QualityFlow: An agentic workflow for program synthesis controlled by LLM quality checks](https://arxiv.org/abs/2501.01234) | 2025 |
| [MARCO: Multi-Agent Code Optimization with Real-Time Knowledge Integration for High-Performance Computing](https://arxiv.org/abs/2505.03906) | 2025 |
| [Hallucination to consensus: Multi-agent LLMs for end-to-end test generation with accurate oracles](https://arxiv.org/abs/2501.11223) | 2025 |
| [MAGE: A multi-agent engine for automated RTL code generation](https://arxiv.org/abs/2406.03554) | DAC 2025 |

#### Blackboard / Shared-State Representation

| Paper | Venue |
| --- | --- |
| [The Hearsay-II Speech-Understanding System: Integrating Knowledge to Resolve Uncertainty](https://doi.org/10.1145/356810.356816) | CSUR 1980 |
| [L2MAC: Large language model automatic computer for extensive code generation](https://arxiv.org/abs/2310.02003) | ICLR 2024 |
| [Gamegpt: Multi-agent collaborative framework for game development](https://arxiv.org/abs/2310.08067) | 2023 |
| [Cogito, ergo sum: A neurobiologically-inspired cognition-memory-growth system for code generation](https://arxiv.org/abs/2501.03456) | 2025 |

### 🎯 Harness-State Convergence

How a multi-agent code system decides the shared harness has reached an acceptable final state.

#### Correctness Convergence (Test-Gated)

| Paper | Venue |
| --- | --- |
| [Agentcoder: Multi-agent-based code generation with iterative testing and optimisation](https://arxiv.org/abs/2312.13010) | 2023 |
| [L2MAC: Large language model automatic computer for extensive code generation](https://arxiv.org/abs/2310.02003) | ICLR 2024 |
| [Hallucination to consensus: Multi-agent LLMs for end-to-end test generation with accurate oracles](https://arxiv.org/abs/2501.11223) | 2025 |

#### Security Convergence

| Paper | Venue |
| --- | --- |
| [AutoSafeCoder: A multi-agent framework for securing LLM code generation through static analysis and fuzz testing](https://arxiv.org/abs/2402.04486) | 2024 |

#### Performance Convergence

| Paper | Venue |
| --- | --- |
| [MARCO: Multi-Agent Code Optimization with Real-Time Knowledge Integration for High-Performance Computing](https://arxiv.org/abs/2505.03906) | 2025 |

#### Score-Based Convergence

| Paper | Venue |
| --- | --- |
| [MAGE: A multi-agent engine for automated RTL code generation](https://arxiv.org/abs/2406.03554) | DAC 2025 |
| [CodeCoR: An LLM-based self-reflective multi-agent framework for code generation](https://arxiv.org/abs/2501.05678) | 2025 |
| [Trae Agent: An LLM-based Agent for Software Engineering with Test-time Scaling](https://arxiv.org/abs/2507.23370) | 2025 |

#### Consensus Convergence

| Paper | Venue |
| --- | --- |
| [QualityFlow: An agentic workflow for program synthesis controlled by LLM quality checks](https://arxiv.org/abs/2501.01234) | 2025 |

#### Implicit Convergence

| Paper | Venue |
| --- | --- |
| [ChatDev: Communicative Agents for Software Development](https://doi.org/10.18653/v1/2024.acl-long.810) | ACL 2024 |
| [MetaGPT: Meta Programming for A Multi-Agent Collaborative Framework](https://openreview.net/forum?id=VtmBAGCN7o) | ICLR 2024 |

## 🚀 Applications and Emerging Fields

Code-centric agentic systems become operational in tangible domains where code defines observable state, executable actions, persistent memory, and feedback signals.

### 💻 Code Assistants

Repositories, tests, issue threads, and development tools form a persistent program world; assistants act over it as code-centric agents.

#### The Repository as a Persistent Program World

| Paper | Venue |
| --- | --- |
| [CodexGraph: Bridging Large Language Models and Code Repositories via Code Graph Databases](https://arxiv.org/abs/2408.03910) | NAACL 2024 |

#### Agent Harnesses as Executable Development Interfaces

| Paper | Venue |
| --- | --- |
| [The openhands software agent sdk: A composable and extensible foundation for production agents](https://arxiv.org/abs/2511.03690) | 2025 |
| [AutoHarness: improving LLM agents by automatically synthesizing a code harness](https://arxiv.org/abs/2603.03329) | 2026 |
| [Agentic Harness Engineering: Observability-Driven Automatic Evolution of Coding-Agent Harnesses](https://arxiv.org/abs/2604.25850) | 2026 |
| [Building Effective AI Coding Agents for the Terminal: Scaffolding, Harness, Context Engineering, and Lessons Learned](https://arxiv.org/abs/2603.05344) | 2026 |

#### Execution Feedback as Grounded Verification

| Paper | Venue |
| --- | --- |
| [Agentless: Demystifying LLM-based Software Engineering Agents](https://arxiv.org/abs/2407.01489) | 2024 |
| [Live-SWE-agent: Can Software Engineering Agents Self-Evolve on the Fly?](https://arxiv.org/abs/2511.13646) | 2025 |
| [Code Generation with AlphaCodium: From Prompt Engineering to Flow Engineering](https://arxiv.org/abs/2401.08500) | 2024 |

#### Memory and Context Management at Repository Scale

| Paper | Venue |
| --- | --- |
| [RepoAgent: An LLM-Powered Open-Source Framework for Repository-level Code Documentation Generation](https://aclanthology.org/2024.emnlp-demo.46/) | EMNLP 2024 Demo |

#### Developer Intent and Project Conventions as Latent State

| Paper | Venue |
| --- | --- |
| [Learning to Commit: Generating Organic Pull Requests via Online Repository Memory](https://arxiv.org/abs/2603.26664) | 2026 |
| [CodeTaste: Can LLMs Generate Human-Level Code Refactorings?](https://arxiv.org/abs/2603.04177) | 2026 |
| [Swe-bench+: Enhanced coding benchmark for llms](https://arxiv.org/abs/2410.06992) | ICSE Companion 2025 |

#### From Inline Completion to Autonomous SWE Agents

| Paper | Venue |
| --- | --- |
| [Evaluating large language models trained on code](https://arxiv.org/abs/2107.03374) | 2021 |
| [The Impact of AI on Developer Productivity: Evidence from GitHub Copilot](https://arxiv.org/abs/2302.06590) | 2023 |
| [Expectation vs.\ Experience: Evaluating the Usability of Code Generation Tools Powered by Large Language Models](https://doi.org/10.1145/3491101.3519665) | CHI Extended Abstracts 2022 |
| [Reading Between the Lines: Modeling User Behavior and Costs in AI-Assisted Programming](https://arxiv.org/abs/2210.14306) | CHI 2024 |

#### From Patch Generation to Software Lifecycle Participation

| Paper | Venue |
| --- | --- |
| [Swe-bench: Can language models resolve real-world github issues?](https://arxiv.org/abs/2310.06770) | ICLR 2023 |
| [SWE-lancer: Can frontier LLMs earn \$1 million from real-world freelance software engineering?](https://arxiv.org/abs/2502.12115) | ICML 2025 |
| [Swe-bench pro: Can ai agents solve long-horizon software engineering tasks?](https://arxiv.org/abs/2509.16941) | 2025 |
| [AI Augmented CI/CD Pipelines: From Code Commit to Production with Autonomous Decisions](http://dx.doi.org/10.1109/FLLM67465.2025.11391007) | 2025 3rd International Conference on Foundation and Large Language Models (FLLM) 2025 |
| [Advances and Frontiers of LLM-based Issue Resolution in Software Engineering: A Comprehensive Survey](https://arxiv.org/abs/2601.11655) | 2026 |

#### Multi-Agent Code Assistance and Shared Repositories

| Paper | Venue |
| --- | --- |
| [ChatDev: Communicative Agents for Software Development](https://doi.org/10.18653/v1/2024.acl-long.810) | ACL 2024 |
| [MetaGPT: Meta Programming for A Multi-Agent Collaborative Framework](https://openreview.net/forum?id=VtmBAGCN7o) | ICLR 2024 |

### 🖥️ GUI / OS Agents

GUI/OS environments are program worlds in the most literal sense: every observation is rendered code, and every action is a call into another piece of code.

#### GUI/OS as a Partially Observable Program World

| Paper | Venue |
| --- | --- |
| [WebArena: A Realistic Web Environment for Building Autonomous Agents](https://arxiv.org/abs/2307.13854) | ICLR 2023 |
| [Mind2Web: Towards a Generalist Agent for the Web](https://arxiv.org/abs/2306.06070) | NeurIPS 2023 |
| [AndroidWorld: A Dynamic Benchmarking Environment for Autonomous Agents](https://arxiv.org/abs/2405.14573) | ICLR 2024 |
| [Windows Agent Arena: Evaluating Multi-Modal OS Agents at Scale](https://arxiv.org/abs/2409.08264) | ICML 2025 |
| [Agentoccam: A simple yet strong baseline for llm-based web agents](https://arxiv.org/abs/2410.13825) | ICLR 2024 |
| [GPT-4V(ision) is a Generalist Web Agent, if Grounded](https://arxiv.org/abs/2401.01614) | ICML 2024 |
| [WebVoyager: Building an End-to-End Web Agent with Large Multimodal Models](https://arxiv.org/abs/2401.13919) | ACL 2024 |
| [OSWorld: Benchmarking Multimodal Agents for Open-Ended Tasks in Real Computer Environments](https://arxiv.org/abs/2404.07972) | NeurIPS 2024 |
| [Set-of-Mark Prompting Unleashes Extraordinary Visual Grounding in GPT-4V](https://arxiv.org/abs/2310.11441) | 2023 |
| [WorkArena: How Capable Are Web Agents at Solving Common Knowledge Work Tasks?](https://arxiv.org/abs/2403.07718) | ICML 2024 |
| [CogAgent: A Visual Language Model for GUI Agents](https://arxiv.org/abs/2312.08914) | Computer Vision and Pattern Recognition 2023 |

#### Unifying Perception, Action, and Evaluation Through Code

| Paper | Venue |
| --- | --- |
| [Executable Code Actions Elicit Better LLM Agents](https://arxiv.org/abs/2402.01030) | ICML 2024 |
| [Cradle: Empowering Foundation Agents Towards General Computer Control](https://arxiv.org/abs/2403.03186) | ICML 2025 |
| [TheAgentCompany: Benchmarking LLM Agents on Consequential Real World Tasks](https://arxiv.org/abs/2412.14161) | 2025 |
| [SeeClick: Harnessing GUI Grounding for Advanced Visual GUI Agents](https://arxiv.org/abs/2401.10935) | ACL 2024 |
| [Ferret-UI: Grounded Mobile UI Understanding with Multimodal LLMs](https://arxiv.org/abs/2404.05719) | ECCV 2024 |
| [OS-ATLAS: A Foundation Action Model for Generalist GUI Agents](https://arxiv.org/abs/2410.23218) | ICLR 2025 |
| [ShowUI: One Vision-Language-Action Model for GUI Visual Agent](https://arxiv.org/abs/2411.17465) | Computer Vision and Pattern Recognition 2024 |
| [Aria-UI: Visual Grounding for GUI Instructions](https://arxiv.org/abs/2412.16256) | ACL 2025 Findings |
| [Navigating the Digital World as Humans Do: Universal Visual Grounding for GUI Agents](https://arxiv.org/abs/2410.05243) | ICLR 2024 |
| [UI-TARS: Pioneering Automated GUI Interaction with Native Agents](https://arxiv.org/abs/2501.12326) | 2025 |
| [GUI-Libra: Training Native GUI Agents to Reason and Act with Action-aware Supervision and Partially Verifiable RL](https://arxiv.org/abs/2602.22190) | 2026 |
| [Spider2-V: How Far Are Multimodal Agents From Automating Data Science and Engineering Workflows?](https://arxiv.org/abs/2407.10956) | NeurIPS 2024 |

#### Memory as Persistent Program State

| Paper | Venue |
| --- | --- |
| [Synapse: Trajectory-as-Exemplar Prompting with Memory for Computer Control](https://arxiv.org/abs/2306.07863) | ICLR 2023 |
| [AppAgent: Multimodal Agents as Smartphone Users](https://arxiv.org/abs/2312.13771) | CHI 2023 |
| [Mobile-Agent-v2: Mobile Device Operation Assistant with Effective Navigation via Multi-Agent Collaboration](https://arxiv.org/abs/2406.01014) | NeurIPS 2024 |
| [UI-Voyager: A Self-Evolving GUI Agent Learning via Failed Experience](https://arxiv.org/abs/2603.24533) | 2026 |
| [AutoGLM: Autonomous Foundation Agents for GUIs](https://arxiv.org/abs/2411.00820) | 2024 |
| [OS-Genesis: Automating GUI Agent Trajectory Construction via Reverse Task Synthesis](https://arxiv.org/abs/2412.19723) | ACL 2024 |

#### UI Simulators and Sandboxes as Executable Dynamics

| Paper | Venue |
| --- | --- |
| [Reinforcement Learning on Web Interfaces Using Workflow-Guided Exploration](https://arxiv.org/abs/1802.08802) | ICLR 2018 |
| [WebShop: Towards Scalable Real-World Web Interaction with Grounded Language Agents](https://arxiv.org/abs/2207.01206) | NeurIPS 2022 |
| [VisualWebArena: Evaluating Multimodal Agents on Realistic Visual Web Tasks](https://arxiv.org/abs/2401.13649) | ACL 2024 |
| [Understanding the Weakness of Large Language Model Agents within a Complex Android Environment](https://arxiv.org/abs/2402.06596) | KDD 2024 |
| [AndroidLab: Training and Systematic Benchmarking of Android Autonomous Agents](https://arxiv.org/abs/2410.24024) | ACL 2025 |
| [AgentBench: Evaluating LLMs as Agents](https://arxiv.org/abs/2308.03688) | ICLR 2023 |
| [Code2World: A GUI World Model via Renderable Code Generation](https://arxiv.org/abs/2602.09856) | 2026 |

#### From Simulation to Production: Executable Feedback Loops

| Paper | Venue |
| --- | --- |
| [3.5 Models and Computer Use](https://www.anthropic.com/news/3-5-models-and-computer-use) | 2024 |
| [Introducing Operator](https://openai.com/index/introducing-operator/) | Blog post |
| [Project Mariner](https://deepmind.google/models/project-mariner/) | 2025 |
| [AutoWebGLM: A Large Language Model-based Web Navigating Agent](https://arxiv.org/abs/2404.03648) | KDD 2024 |

### 🔬 Scientific Discovery Agents

Hypotheses are encoded as differential equations or generative models; protocols as XDL or Opentrons scripts; analyses as Jupyter notebooks. Code carries scientific reasoning, scientific action, and the scientific environment itself.

#### Scientific Discovery as a Partially Observable Program World

| Paper | Venue |
| --- | --- |
| [The AI Scientist-v2: Workshop-Level Automated Scientific Discovery via Agentic Tree Search](https://arxiv.org/abs/2504.08066) | 2025 |
| [ChemCrow: Augmenting large-language models with chemistry tools](https://arxiv.org/abs/2304.05376) | Nature 2023 |

#### Unifying Ideation, Experimentation, Analysis, and Communication

| Paper | Venue |
| --- | --- |
| [ResearchAgent: Iterative Research Idea Generation over Scientific Literature with Large Language Models](https://arxiv.org/abs/2404.07738) | NAACL 2024 |
| [BioPlanner: Automatic Evaluation of LLMs on Protocol Planning in Biology](https://arxiv.org/abs/2310.10632) | EMNLP 2023 |
| [Agent Laboratory: Using LLM Agents as Research Assistants](https://arxiv.org/abs/2501.04227) | EMNLP 2025 Findings |
| [AgentRxiv: Towards Collaborative Autonomous Research](https://arxiv.org/abs/2503.18102) | 2025 |
| [The AI Scientist: Towards Fully Automated Open-Ended Scientific Discovery](https://arxiv.org/abs/2408.06292) | 2024 |
| [Towards Scientific Intelligence: A Survey of LLM-based Scientific Agents](https://arxiv.org/abs/2503.24047) | 2026 |
| [Executable Code Actions Elicit Better LLM Agents](https://arxiv.org/abs/2402.01030) | ICML 2024 |

#### Memory as Persistent Program State

| Paper | Venue |
| --- | --- |
| [AIDE: AI-Driven Exploration in the Space of Code](https://arxiv.org/abs/2502.13138) | 2025 ⚠️ link mismatch |
| [El Agente: An autonomous agent for quantum chemistry](http://dx.doi.org/10.1016/j.matt.2025.102263) | Matter 2025 |
| [PaperQA: Retrieval-Augmented Generative Agent for Scientific Research](https://arxiv.org/abs/2312.07559) | 2023 |
| [Towards an AI co-scientist](https://arxiv.org/abs/2502.18864) | 2025 |

#### Simulators as Executable Dynamics

| Paper | Venue |
| --- | --- |
| [AlphaEvolve: A coding agent for scientific and algorithmic discovery](https://arxiv.org/abs/2506.13131) | 2025 |

#### Self-Driving Labs as Executable Feedback Loops

| Paper | Venue |
| --- | --- |
| [Self-driving laboratory for accelerated discovery of thin-film materials](https://arxiv.org/abs/1906.05398) | Science 2019 |
| [MatPilot: an LLM-enabled AI Materials Scientist under the Framework of Human-Machine Collaboration](https://arxiv.org/abs/2411.08063) | 2024 |

#### Toward Agentic and Instruction-Following Science

| Paper | Venue |
| --- | --- |
| [MLAgentBench: Evaluating Language Agents on Machine Learning Experimentation](https://arxiv.org/abs/2310.03302) | ICML 2023 |
| [MLE-bench: Evaluating Machine Learning Agents on Machine Learning Engineering](https://arxiv.org/abs/2410.07095) | ICLR 2025 |
| [A Survey of Scientific Large Language Models: From Data Foundations to Agent Frontiers](https://arxiv.org/abs/2508.21148) | 2025 |
| [ScienceAgentBench: Toward Rigorous Assessment of Language Agents for Data-Driven Scientific Discovery](https://arxiv.org/abs/2410.05080) | ICLR 2025 |
| [DiscoveryBench: Towards Data-Driven Discovery with Large Language Models](https://arxiv.org/abs/2407.01725) | ICLR 2024 |

### 🤖 Autonomous Embodied Agents

Code grounds embodied actions in physical feasibility, accumulates reusable skills as memory, and supports auditable real-world deployment.

#### Agent Harness for Grounded and Verifiable Embodied Actions

| Paper | Venue |
| --- | --- |
| [Do as i can, not as i say: Grounding language in robotic affordances](https://arxiv.org/abs/2204.01691) | CoRL 2022 |
| [Robots that ask for help: Uncertainty alignment for large language model planners](https://arxiv.org/abs/2307.01928) | CoRL 2023 |
| [SkillVLA: Tackling Combinatorial Diversity in Dual-Arm Manipulation via Skill Reuse](https://arxiv.org/abs/2603.03836) | 2026 |
| [Bootstrap your own skills: Learning to solve new tasks with large language model guidance](https://arxiv.org/abs/2310.10021) | CoRL 2023 |
| [Robocodex: Multimodal code generation for robotic behavior synthesis](https://arxiv.org/abs/2402.16117) | ICML 2024 |
| [LLM-Driven Corrective Robot Operation Code Generation with Static Text-Based Simulation](https://arxiv.org/abs/2512.02002) | 2025 |
| [NormCode: A Semi-Formal Language for Auditable AI Planning](https://arxiv.org/abs/2512.10563) | 2025 |
| [Cp-agent: Agentic constraint programming](https://arxiv.org/abs/2508.07468) | 2025 |
| [Veriguard: Enhancing llm agent safety via verified code generation](https://arxiv.org/abs/2510.05156) | 2025 |

#### Reusable Skills as Embodied Memory

| Paper | Venue |
| --- | --- |
| [Growing with your embodied agent: A human-in-the-loop lifelong code generation framework for long-horizon manipulation skills](https://arxiv.org/abs/2509.18597) | 2025 |
| [Vireskill: Vision-grounded replanning with skill memory for llm-based planning in lifelong robot learning](https://arxiv.org/abs/2509.24219) | 2025 |
| [UI-Voyager: A Self-Evolving GUI Agent Learning via Failed Experience](https://arxiv.org/abs/2603.24533) | 2026 |

#### Coordinated and Auditable Real-World Deployment

| Paper | Venue |
| --- | --- |
| [RACAS: Controlling Diverse Robots With a Single Agentic System](https://arxiv.org/abs/2603.05621) | 2026 |
| [ALRM: Agentic LLM for Robotic Manipulation](https://arxiv.org/abs/2601.19510) | 2026 |

### 🎬 Agent Personalization (Recommender Systems)

Recommender systems instantiate the program-world abstraction at scale: user state evolves, policies are executable procedures, and feedback closes the loop through executable data, policy, and evaluation pipelines.

*(This subsection of the survey provides a conceptual reframing without explicit citations beyond cross-references; see other sections for related papers.)*

---

## ✨ Acknowledgements

We thank the broader community for the contributions surveyed here. If your paper should be added or moved, please open a pull request or issue.

## 📄 License

This repository is released under the [MIT License](LICENSE).