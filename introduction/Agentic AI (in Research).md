# Agentic AI (in Research)
## Overview over Concepts, News and Trends in Agentic AI (in Research)

Philip Müller | 08.06.2026 | HAICON 2026
<!-- slide template="[[title-slide]]" -->

---

<!-- slide template="[[section-slide]]" -->
::: sectiontitle
# Introduction & Motivation
::: 

---

### What is an agent really?
* **Working Definition**: system that autonomously plans, acts, and iterates using tools to achieve a goal
* an Agent is **NOT** LLM + single tool call
* Canonical Loop: Goal → Plan → Act → Observe → Repeat
* *Core Properties*
  - **Goal-directed behavior**  
      Works toward an explicit objective
  - **Decision-making**  
      Chooses next actions based on intermediate results
  - **Iteration (loop)**  
      Refines outputs over multiple steps

---

### Use Cases of Gen AI in Research
* Witte, J., Bayer, S., Weber, I. (2026) [_Use Cases for the Application of Generative Artificial Intelligence for Researchers: A Survey_](https://hal.science/hal-05463006) 
* List 118 potential Use Cases of Gen AI across 6 categories:
  - **Ideation** (hypothesis generation)
  - **Literature Review** (search, summarization)
  - **Methodology** (design support)
  - **Data Collection** (extraction, labeling)
  - **Programming** (code generation, debugging)
  - **Data** Analysis (exploration, visualization)
  - **Writing** (drafting, editing, formatting)

---

### Persistent agents are emerging
* Early LLMs were largely stateless: prompt → response → context lost
* New systems increasingly retain project relevant knowledge, goals, tasks, preferences 

**Persistent agents**
* Operate across sessions and restarts
* Resume previous work automatically
* Maintain evolving context about users and projects
* Can monitor systems and perform long-running workflows

**Observation**
* interaction model: _asking questions_ → _delegating responsibilities_
* unit of interaction: _prompt_ → _project_

---

### Agent Harnesses Are Becoming the New Operating Layer
* Performance increasingly depends on orchestration rather than model capability alone
* **Harnesses** = software infrastructure layer wrapped around an AI model
  * Planning + decomposition
  * Context Management, Memory access and retrieval
  * Tool routing and execution
  * Verification and retry loops
  * Multi-step control flow across agents

**Observation**: _model-centric AI_ → _system-centric AI_

---

### Data, Memory, and Context Layers Are Becoming as Important as Models
* top-tier frontier models are increasingly comparable on many benchmarks ([LLM Leaderboard 2026: 20 Models Ranked by MMLU, HumanEval & GPQA](https://precisionaiacademy.com/llm-leaderboard))
* Long-horizon agents require persistent external state beyond context windows

**Core mechanisms**
* Retrieval (RAG) over static prompting
* Persistent memory stores (project / user history)
* Context compression & summarization pipelines
* External knowledge bases linked to agents
  * [Kaparthy's llm-wiki](https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f)

---

### MCP Became the USB-C of AI Tools
* Model Context Protocol (MCP) standardizes how models connect to tools and external systems
* Built on simple structured messaging patterns (JSON-RPC-like design)
* Rapid ecosystem adoption: “everything gets an MCP server”
* Tool layer becomes composable and interchangeable
* Protocol is rapidly advancing ([MCP Is Growing Up - Agentic AI Foundation (AAIF)](https://aaif.io/blog/mcp-is-growing-up/))
* Some issues remain (high context-token usage)

---

![](assets/mcp_adaption.avif)
---

### The New Design Paradigm Is Visual and Agentic
* Text-only interaction is reaching its limits for complex outputs, multi-step workflows and user-interaction
* AI systems increasingly generate interactive UI, not just text outputs

**MCP Apps**
* Interactive UI applications rendered inside clients (e.g. Claude Desktop)
* MCP servers can return structured HTML-based interfaces
* Enables forms, dashboards, data exploration, and tool-driven interaction inside chat environments
---

<!-- slide template="[[wide-slide]]" -->
<img  src="https://github.com/excalidraw/excalidraw-mcp/blob/main/docs/demo.gif?raw=true"  
controls  style="width:100%; height:auto; display: flex; justify-self: center;" />
https://github.com/excalidraw/excalidraw-mcp

---
### The New Design Paradigm Is Visual and Agentic (2)

Provider-Specific implementations
* [Claude Artifacts](https://support.claude.com/en/articles/9487310-what-are-artifacts-and-how-do-i-use-them) %% https://www.youtube.com/watch?v=Ii99RU3mOJM %%
* [OpenAI Canvas](https://help.openai.com/en/articles/9930697-what-is-the-canvas-feature-in-chatgpt-and-how-do-i-use-it)
* [Google Gemini Canvas](https://gemini.google/overview/canvas/)
* [CopilotKit Open Generative UI](https://github.com/CopilotKit/OpenGenerativeUI)
* [Omma](https://omma.build/)

---

<!-- slide template="[[wide-slide]]" -->
<video  
src="https://github.com/user-attachments/assets/ed28c734-e54e-4412-873f-4801da544a7f"  
controls  style="width:100%; height:auto; display: flex; justify-self: center;">  
</video>
Example of interactive visualization created with Open Generative UI

---

![](assets/kaparthy_visual_paradigm.avif)
[Karpathy about Paradigm Shift in Output Format](https://x.com/karpathy/status/2053872850101285137)

---

<!-- slide template="[[wide-slide]]" -->
#### OAuth Was Built for Apps — Now It Must Handle Agents

![](assets/agent_authentication.avif)

---

### OAuth Was Built for Apps — Now It Must Handle Agents
* Agents increasingly perform user-specific actions
* Existing mechanisms like OAuth are being extended into contexts they were not originally designed for
* Authentication and authorization systems were designed for human-driven, app-centric workflows
* Agents operate on behalf of users, but lack a stable, first-class identity model in the internet stack
* Identity, permissions, and accountability for agents remain fundamentally unresolved

---

<!-- slide template="[[section-slide]]" -->
::: sectiontitle
# Trends
::: 

---
### Agents Are Slowly Entering Everyday Infrastructure
* Beyond general-purpose assistants, agentic systems are increasingly being deployed as domain-specific infrastructure
* Providers are moving from consumer tools → institutional and sector-specific deployments
* These systems are no longer just productivity tools, but embedded operational components of real-world institutions

---

### Agents Are Slowly Entering Everyday Infrastructure

**Examples of deployment domains**
* Design workflows and creative tooling pipelines
* Healthcare support systems (clinical assistance, workflow automation, documentation)
* Education systems (tutoring, grading support, personalized learning environments)

---

### Small Models Are Moving Agentic AI to the Edge
* Push toward on-device agentic systems instead of cloud-only execution
* Driven by latency, privacy, cost, and always-available agents
* Karpathy: “~1B parameter cognitive core may be sufficient” ([source](https://www.youtube.com/watch?v=UldqWmyUap4))
* Newer Models by major providers going very small, built natively for on-device, mobile, and browser environments
* Gemma 4: smallest tier [~2B](https://blog.google/innovation-and-ai/technology/developers-tools/gemma-4/)
* Gemma 3: smallest tier [~270M](https://developers.googleblog.com/en/introducing-gemma-3-270m/)
* Qwen3.5 models down to ~0.8B parameters

---

<!-- slide template="[[wide-slide]]" -->
<split even>
<img width="480" src="https://github.com/user-attachments/assets/a809ad78-aef4-4169-91ee-de7213cbb3bd" style="object-fit: scale-down !important;" />
<img width="480" src="https://github.com/user-attachments/assets/1effd10d-f45a-4f7b-9435-f50f1bdd36b6"style="object-fit: scale-down; !important" />
<img width="480" src="https://github.com/user-attachments/assets/061564ed-030f-4630-810b-13a7863fce4c" style="object-fit: scale-down; !important"/>
</split>

#### Google AI Edge Gallery: Gemma models on mobile
---

<!-- slide template="[[wide-slide]]" -->

<img src="https://developers.google.com/static/coral/images/Coralboard-Synap-transparent-finger_960.png" style="height: 600px;"/>
<h4>Google Coralboard</h4>
<span>source: <a href="https://developers.google.com/coral/products">https://developers.google.com/coral/products</a></span>

---

<!-- slide template="[[wide-slide]]" -->
![](assets/google_chrome_gemini_nano.avif)
<span>source: https://www.thatprivacyguy.com/blog/chrome-silent-nano-install/</span>

---

### Agents Already Operate at Superhuman Scale
* [Peter Steinberger](https://x.com/steipete/status/2055346265869721905)
  * ~100 Codex agents running continuously 
  * spending tokens worth ~1.3 million dollars for the month
* [Microsoft MDASH](https://www.microsoft.com/en-us/security/blog/2026/05/12/defense-at-ai-speed-microsofts-new-multi-model-agentic-security-system-tops-leading-industry-benchmark/)
  * "Microsoft’s new multi-model agentic security system"
  * 100 agents orchestrated for vulnerability discovery
  * agents challenge and verify one another

---

### Agents Already Operate at Superhuman Scale (2)
* [Cursor FastRender](https://github.com/wilsonzlin/fastrender)
  * official Cursor research project, where agentic swarms developed browser rendering engine 
    * browsers are considered among the most complex pieces of software to develop
    * but also among the best specified
  * ran hundreds to thousands of frontier-model agents
  * project has >30.000 commits

---

### Agents Already Operate at Superhuman Scale (3)
* Google Antigravity building an OS from Scratch using ["93 subagents, 15,314 model calls, and over 339M input tokens"](https://antigravity.google/blog/google-antigravity-built-an-os)
* [Qwen3.7-Max](https://qwen.ai/blog?id=qwen3.7)
  * wrote, compiled, profiled and optimized a complex hardware architecture kernel entirely on its own 
  * ran conituously over 35 hours, executing 1,158 tool calls across 432 kernel evaluations

---

### Multi-Agent Systems Are Becoming the Dominant Pattern
* Complex tasks are increasingly decomposed across multiple specialized agents
* Example: Planner → Worker → Reviewer
* Industry Examples
	* Microsoft MDASH (>100 security agents)
	- Cloudflare vulnerability discovery harness
	- Anthropic Code Review (parallel reviewer agents)
	- OpenAI Codex ("Designed for multi-agent workflows")
* **Paperclip**: models software organizations as teams of specialized agents (e.g. engineering, product, design, review), coordinated through structured workflows rather than a single agent

---

### AI Training Itself Is Becoming Agentic
* [autoresearch](https://github.com/karpathy/autoresearch) by Kaparthy
  * demonstrates autonomous, self-improving AI agents
  * agents are used to implement small iterative experiments for optimization
  * Hypothesis → Experiment → Evaluation → Repeat
* [ml-intern](https://github.com/huggingface/ml-intern) by HuggingFace
  * "reads papers, finds datasets, trains models, and iterates until the numbers go up"
  * in tests, [generated synthetic data points, upsampled and trained on it, outperforming baseline](https://www.linkedin.com/feed/update/urn:li:activity:7452298087814995968/)

---

### AI Training Itself Is Becoming Agentic (2)
* Kaparthy moves to Anthropic to [build a team that uses Claude to accelerate model development itself](https://www.trendingtopics.eu/ki-groesse-und-openai-mitgruender-andrej-karpathy-geht-zu-anthropic-um-claude-zu-verbessern/)
* AI Startup [Recursive](https://www.recursive.com/) emerges with [$4.65 billion valuation](https://www.finsmes.com/2026/05/recursive-superintelligence-raises-650m-in-funding-at-4-65-billion-valuation.html), aiming to build AI systems that recursively improve themselves
* Qwen-Team integrated Qwen3.7-Max into the Reinforcement Learning (RL) monitoring 
  * model acted as reward hacking self-monitoring and rule self-evolution
  * systematically identified candidate hacking patterns, performed rule verification, counter-example mining, and iterative optimization

---
### Open Research Questions
Agentic AI Still Faces Fundamental Research Challenges:
- **Context Drift**: Losing focus during long workflows
- **Reliable Planning**: Breaking tasks into effective steps
- **Tool Use**: Robustly selecting and using tools
- **Human Oversight Does not Scale**: Outputs exceed human review capacity
	- → The New Bottleneck Is Verification, Not Generation
- **Verification**: Proving outputs are correct
	- **Reward Hacking**: Optimizing metrics instead of objectives
- **Benchmarks Are Becoming Increasingly Controversial**: Measuring real-world agent performance
- **Continuous Learning**: Learning without forgetting

---
<!-- slide template="[[section-slide]]" -->
::: sectiontitle
# Open Source & Security 
::: 

---

%%
https://webmatrices.com/app-ideas/ai-pr-author-scrutiny 
https://removepaywalls.com/https://blog.devgenius.io/open-source-projects-are-now-banning-ai-generated-pull-requests-8e1dd3e8d41c 
[RFC 406i The Rejection of Artificially Generated Slop](406.fail) 
https://daniel.haxx.se/blog/2025/07/14/death-by-a-thousand-slops/
%%
### Generative AI Is Stress-Testing Open Source Communities
* "AI slop is DDoSing open source" - Daniel Stenberg (`cURL`) via [thenewstack](https://thenewstack.io/curls-daniel-stenberg-ai-is-ddosing-open-source-and-fixing-its-bugs/)
  * increasing number of bug reports in cURL’s bug bounty program were AI-generated
  * at one point volume spiked to 8x the usual rate

---
### Generative AI Is Stress-Testing Open Source Communities
* [13,000-line AI-generated PR](https://github.com/ocaml/ocaml/pull/14369#issuecomment-3556593972) at OCaml
  * Coding Agents incorrectly credited Mark Shinwell ([oxcaml](https://github.com/oxcaml/oxcaml)) in the [file headers](https://github.com/ocaml/ocaml/pull/14369/changes)
    * Author responsed with a lengthy "AI-written copyright analysis"
    * asked directly Author responded "Beats me. AI decided to do so and I didn't question it." [source](https://github.com/ocaml/ocaml/pull/14369#issuecomment-3557357958)
  * maintainers rejected the PR request
    * "AI-written code is more taxing that reviewing human-written code"
    * "creates a very real risk of bringing the Pull-Request system to a halt"
  * [devclass.com](https://www.devclass.com/ai-ml/2025/11/27/ocaml-maintainers-reject-massive-ai-generated-pull-request/1728083) reported on it
    * incorrectly stated that Mark Shinwell was involved in the discussion
    * this spread to reddit and other forums

---

<!-- slide template="[[wide-slide]]" -->
![](assets/ocaml_repo_commits.avif)

--
<!-- slide template="[[wide-slide]]" -->

![](assets/ocaml_pr_vibe_coded.avif)

--
<!-- slide template="[[wide-slide]]" -->

![](assets/ocaml_mark_shinwell_credited.avif)

--
<!-- slide template="[[wide-slide]]" -->

![](assets/ocaml_ai_written_copyright_analysis.avif)

--
<!-- slide template="[[wide-slide]]" -->

![](assets/ocaml_beats_me.avif)



---



%%
https://www.anthropic.com/glasswing
https://the-decoder.de/mozilla-setzt-anthropics-claude-mythos-ein-und-behebt-hunderte-sicherheitsprobleme-in-firefox/
%%
### AI Agents Are Becoming Cybersecurity Actors
* Frontier models [Claude Mythos Preview and GPT-5.5](https://www.aisi.gov.uk/blog/our-evaluation-of-openais-gpt-5-5-cyber-capabilities) can autonomously discover vulnerabilities, develop exploits, and execute end-to-end attack chains.
* These capabilities lower the skill barrier for advanced cyberattacks and increase the scalability of exploitation.
* [Project Glasswing](https://www.anthropic.com/research/glasswing-initial-update) shows systematic vulnerability discovery at scale
  * Mozilla alone reported 271 Firefox vulnerabilities found in a single pass, including long-standing bugs.
* While current frontier deployments are limited to major labs and select partners, the underlying capabilities generalize and pose growing risk to smaller, less-resourced projects and organizations.

%% https://simonwillison.net/2026/May/7/firefox-claude-mythos/ %%

---

<!-- slide template="[[section-slide]]" -->
::: sectiontitle
# Economics & Ecosystem
::: 

---

%%
https://the-decoder.de/das-erste-ki-labor-in-den-schwarzen-zahlen-heisst-anthropic/
https://www.spiceworks.com/ai/token-shock-and-the-hidden-cost-of-ai-consumption/
%%

### The Cost Explosion Everybody Expected

* Agentic workflows consume massive amounts of tokens due to multi-step reasoning and tool calls
* Inference costs are predicted to drop strongly over time ([›90% by 2030 for large models](https://www.gartner.com/en/newsroom/press-releases/2026-03-25-gartner-predicts-that-by-2030-performing-inference-on-an-llm-with-1-trillion-parameters-will-cost-genai-providers-over-90-percent-less-than-in-2025))
* Agentic workflows put pressure on current pricing models for LLM inference
* Providers are moving from flat-rate pricing to usage-based, token-based billing
  * [GitHub Copilot transitioned to token consumption-based billing](https://github.com/orgs/community/discussions/192948)
* Is the Bubble Bursting?

---

<!-- slide template="[[wide-slide]]" -->
![](assets/Blablador_to_the_Rescue.avif)
### Blablador to the Rescue!

---

<!-- slide template="[[wide-slide]]" -->

![Image from simonwillison.net, Copyright Simon Willison, licensed under Apache License 2.0.](https://static.simonwillison.net/static/2026/5-minutes-llms/5-minutes-llms.026.jpeg)
<div style="text-align: center;">
<h4>Local Models Are Becoming Surprisingly Competitive</h4>
<span style="font-size:smaller;"><a href="https://static.simonwillison.net/static/2026/5-minutes-llms/5-minutes-llms.026.jpeg">Image from simonwillison.net, Copyright Simon Willison, licensed under Apache License 2.0.</a>
</span>
</div>

---

### Are Open Weight Models By Major Providers Diminishing?
* The technical lead of Alibaba's Qwen team, Junyang Lin and several key contributors recently stepped down
* this happened only a day after the new Qwen 3.5 open-weight models were released
* Multiple signals suggest Qwen may reduce its emphasis on open-weight releases

---

%%
https://martinalderson.com/posts/open-weights-are-quietly-closing-up/
%%
### Are Open Weight Models By Major Providers Diminishing?
* Frontier labs released open-weight models to drive adoption, build ecosystems, attract talent, and establish market leadership
* Open-weight releases make direct monetization more difficult than API-based access
* Growing competition and rising inference costs increase pressure to generate revenue from model usage
* As revenue pressure grows, the long-term commitment of major providers to open-weight models remains uncertain

---

<!-- slide template="[[section-slide]]" -->
::: sectiontitle
# Research & Society
::: 

---

### Research Agents Are Automating Entire Pipelines
* AI agents are moving beyond literature search and coding assistance toward end-to-end research workflows
* Leading companies already use large numbers of agents for software development, optimization, and AI training
* Similar approaches are being explored for scientific discovery, experimentation, and analysis
* Research may increasingly become a continuous, 24/7 process driven by autonomous systems

---
### Scientific Publishing Is Under Pressure

![](assets/ICML_Submissions.avif)

---

### Scientific Publishing Is Under Pressure
* ICML received roughly 24,000 submissions in 2026, continuing a rapid growth trend
* AI tools make it easier to produce papers, reviews, and research artifacts at scale
* Reviewers face increasing difficulty distinguishing high-quality work from AI-generated "slop"
* Conferences ([ICLR](https://blog.iclr.cc/2025/04/15/leveraging-llm-feedback-to-enhance-review-quality/), [ACLRR](https://arxiv.org/abs/2604.13940), [EMNLP](https://2026.emnlp.org/ai-reviewing-experiment/),...) are already piloting AI-assisted reviewing
* arXiv has introduced [1-year penalty](https://x.com/tdietterich/status/2055000956144935055) for authors submitting low-quality AI-generated content

---

### Research Institutions Are Not Prepared for Autonomous AI
* Regulatory systems were designed for static software, not adaptive autonomous systems acting continuously and at scale.
* research society may require new mechanisms for trust, provenance, and accountability.

---

### Agentic AI Is Not a Future Technology Anymore

The transition is already underway. The key challenge is **shaping how these systems integrate into science, institutions, and society** and **how to regulate them**.
