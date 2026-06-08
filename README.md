# Agentic AI Workshop

A workshop on agentic AI, using the [Abstracts Explorer](https://github.com/thawn/abstracts-explorer) and the [Agentic RAG Hackathon](https://github.com/haider-khan-91/haicon26-agentic-rag-hackathon) as case studies.

Slide PDFs can be found in [releases](https://github.com/Helmholtz-AI-Matter/agentic-ai-workshop/releases).

Use a PDF reader that can play movies (e.g. Adobe Acrobat Reader, Foxit Reader).

## Agenda

### Presentations — Architecture walk-through, live demo, design trade-offs, and lessons learned & Discussion (2 h)

| Time    | Session                                                                                                                                |
| ------- | -------------------------------------------------------------------------------------------------------------------------------------- |
| ~30 min | **Introduction to Agentic AI for Science**                                                                                             |
| ~30 min | **Project Presentation: Abstracts Explorer**                                                                                           |                                                                                                                           |
| ~30 min | **Project Presentation: Voucher Canvas Agent**                                                                                         |
| ~30 min | **General Discussion** — Cross-cutting themes: What design patterns transferred? Where did things break? What would we do differently? |

### Hackathon (2 h)

Participants form small groups to **build or plan** agentic ML tools hands-on. Groups self-organize around topics proposed in the morning discussion. Possible tracks include:

- **Feature sprints** — Implement a concrete feature in one of the presented projects (e.g., a new MCP tool, a conference downloader plugin, an improved clustering pipeline). Bring a laptop and be ready to write code.
- **Project planning** — Sketch the architecture and roadmap for a new agentic tool addressing a participant's own research domain. Output: a brief design document or project proposal.
- **Integration experiments** — Wire up existing tools via MCP or other protocols and stress-test them with real scientific queries.

| Time    | Session                                                                                         |
| ------- | ----------------------------------------------------------------------------------------------- |
| ~15 min | **Group Formation** — Pitch topics, form groups (3–5 people).                                   |
| ~90 min | **Hands-on Work** — Small-group hacking / planning with roaming support from organizers.        |
| ~15 min | **Lightning Reports** — Each group presents what they built, learned, or planned (~2 min each). |

Choose **one** track:

- **[Abstracts Explorer](https://github.com/thawn/abstracts-explorer)** — contribute to a production agentic literature tool
- **[Agentic RAG Hackathon](https://github.com/haider-khan-91/haicon26-agentic-rag-hackathon)** — build, plan, or stress-test a minimal PDF research bot (MCP + simple RAG)

### Abstracts Explorer

Follow the setup instructions in the [Contributing Guide](https://thawn.github.io/abstracts-explorer/contributing.html).

Check out the [good first issues on github](https://github.com/thawn/abstracts-explorer/issues?q=is%3Aissue+is%3Aopen+label%3A%22good+first+issue%22) to choose a task. You can also suggest your own improvements or features by opening an issue.

#### Suggested improvements for Abstracts Explorer

- Improve documentation and setup instructions [issue #375](https://github.com/thawn/abstracts-explorer/issues/375)
- Implement a new conference plugin [issue #380](https://github.com/thawn/abstracts-explorer/issues/380)
- (Advanced) Fix a bug in the search papers MCP tool [issue #369](https://github.com/thawn/abstracts-explorer/issues/369)

### Agentic RAG Hackathon

Hands-on **2 h** mini hackathon over a small public repo: MCP servers, local PDFs, and a four-step research bot (Discover → Select → Read → Answer) — a simple RAG pipeline.

**Repository:** [github.com/haider-khan-91/haicon26-agentic-rag-hackathon](https://github.com/haider-khan-91/haicon26-agentic-rag-hackathon)

Pick **one track** (full instructions in the repo; start with `PARTICIPANT_SHEET.md`):

| Track | Focus |
|-------|--------|
| **A — Feature sprint** | Extend the bot — new MCP tool or pipeline improvement |
| **B — Architecture planning** | Plan agentic integration for your project or another system — no coding |
| **C — Integration experiments** | Stress-test MCP tools, compare tool path vs full bot, report failures |

No API key required for most tasks; optional for full bot runs and some Track A items.
