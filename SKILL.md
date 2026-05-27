---
name: managing-agent-knowledge
description: "MUST be loaded before designing, creating, reviewing, auditing, updating, or maintaining agent-readable knowledge systems, LLM wiki corpora, retrieval bundles, source-cited knowledge bases, or memory architectures. Use when you need to turn source material into durable agent knowledge, separate canonical knowledge from memory, define freshness and citation discipline, design corpus tools, or build retrieval contracts for agents."
---

<objective>
Manage agent-readable knowledge as a durable system: source material is compiled into a maintained corpus, the corpus is kept separate from agent memory, retrieval contracts define what enters context, and validation catches drift before users rely on stale or unsupported claims.

Use this skill for domain-neutral knowledge systems: legal corpora, policy libraries, product knowledge, research wikis, enterprise procedure books, or any source-cited corpus an agent must read, maintain, cite, and traverse reliably.
</objective>

<quick_start>
Classify the user's request, then read the matching workflow:

1. Designing a new corpus or restructuring an existing one: `workflows/design-knowledge-system.md`
2. Adding, updating, or compiling knowledge: `workflows/add-or-update-knowledge.md`
3. Creating retrieval bundles or persona-task contracts: `workflows/build-retrieval-contracts.md`
4. Auditing, repairing, or checking corpus health: `workflows/audit-knowledge-corpus.md`
5. Separating canonical knowledge, private memory, and procedural skills: `workflows/design-memory-boundaries.md`
6. Designing agent-facing corpus tools or output contracts: `workflows/design-knowledge-tools.md`

If the request already gives enough context, do not ask intake questions. Start with the workflow and gather missing facts from the repo or provided material.
</quick_start>

<essential_principles>
**Canonical knowledge is not memory.** Canonical corpus content is externally sourced, versioned, and editorially maintained. Agent inferences, conversation summaries, and tenant/customer preferences never become canonical facts without an explicit source-backed editorial update.

**Source-first, compiled knowledge.** Keep raw sources as the authority. Compile them into concise, traversable Markdown knowledge pages with citations, dates, status, and links. Do not paste raw documents into the corpus as a substitute for synthesis.

**Every page must be readable cold.** An agent may land from search, a tag, a backlink, or a bundle. Concept pages must self-contextualize in the opening sentences. Index pages must orient the reader, not just list links.

**One concept, one canonical home.** Store each durable fact in one authoritative page, then link to it from siblings, use cases, indexes, bundles, and synthesis pages. Duplication creates drift.

**Metadata is part of the product.** Status, freshness dates, source kind, tags, and see-also links are not bookkeeping. They are the control surface agents use to decide whether to answer, warn, refuse, or fetch upstream sources.

**Navigation has multiple axes.** Folders say where editors work. Tags say what a file is about. Inclusion links say what context a file lives inside. Good agent retrieval needs all three.

**Retrieval contracts beat accidental RAG.** For recurring persona-task work, predefine the required files, source articles/sections, tags, freshness window, refusal rules, and citation pattern. Let ad-hoc search handle the long tail.

**Verification is structural.** Important claims should be checked against cited sources by an audit step, verifier, test, or sub-agent with bounded authority. Self-reflection is not enough for high-stakes knowledge.

**Stewardship is continuous.** Freshness decay, broken links, missing citations, claim drift, dead sources, stale bundles, and uncovered user questions should produce an explicit backlog, not disappear into chat history.
</essential_principles>

<intake>
Ask only for gaps that materially affect the structure or authority model. Useful questions:

- What domain and user jobs must this knowledge support?
- Which sources are authoritative, and which are merely background?
- Must agents cite every claim, or only high-impact claims?
- Is this a single shared corpus, a per-tenant corpus, or shared canonical knowledge plus private memory?
- What outputs should exist when the work is done: corpus pages, conventions, bundle specs, audit reports, tools, or evals?
</intake>

<routing>
Use this routing map:

- `design`, `new corpus`, `knowledge base`, `LLM wiki`, `architecture`, `restructure`: read `workflows/design-knowledge-system.md`
- `add`, `update`, `compile`, `distill`, `ingest`, `write knowledge`, `refresh page`: read `workflows/add-or-update-knowledge.md`
- `bundle`, `retrieval contract`, `persona`, `task`, `preload`, `context package`: read `workflows/build-retrieval-contracts.md`
- `audit`, `review corpus`, `review knowledge`, `health`, `stale`, `broken links`, `citations`, `claim drift`, `gaps`: read `workflows/audit-knowledge-corpus.md`
- `memory`, `tenant`, `private notes`, `canonical`, `procedural skill`, `episodic`, `semantic`: read `workflows/design-memory-boundaries.md`
- `tool`, `tool description`, `corpus API`, `MCP`, `SDK tool`, `output envelope`, `TOON`, `structured error`: read `workflows/design-knowledge-tools.md`

After reading the workflow, follow it exactly. Load only the knowledge files listed in that workflow's required reading.
</routing>

<knowledge_index>
All reusable knowledge is in `knowledge/`:

**Architecture:** `corpus-architecture.md`, `writing-patterns.md`, `memory-boundaries.md`
**Metadata and retrieval:** `frontmatter-and-taxonomy.md`, `navigation-and-links.md`, `retrieval-contracts-and-bundles.md`
**Trust and operations:** `source-and-freshness-discipline.md`, `stewardship-and-evals.md`, `tool-and-output-contracts.md`
</knowledge_index>

<templates_index>
Reusable output templates are in `templates/`:

- `content-file.md`: source-cited corpus page template
- `bundle.yaml`: persona-task retrieval contract template
- `audit-report.md`: corpus health report template
- `eval-scenarios.json`: lightweight behavioral eval template
</templates_index>

<workflows_index>
Available workflows:

- `design-knowledge-system.md`: design or restructure an agent-readable corpus
- `add-or-update-knowledge.md`: compile sources into knowledge pages or update existing pages
- `audit-knowledge-corpus.md`: check freshness, links, citations, tags, drift, and gaps
- `build-retrieval-contracts.md`: define persona-task bundles and routing signals
- `design-memory-boundaries.md`: separate canonical knowledge from agent memory and procedural skills
- `design-knowledge-tools.md`: design agent-facing corpus tools, descriptions, and output envelopes
</workflows_index>

<trigger_tests>
Should trigger:

- "Design a knowledge base my agent can cite and maintain."
- "Audit this corpus for stale claims, broken links, and missing source coverage."
- "Turn these project conventions into reusable retrieval bundles and memory rules."

Should not trigger:

- "Summarize this article for a blog post" when no durable agent knowledge system is being created or maintained.
</trigger_tests>

<success_criteria>
The work is successful when:

- The canonical source of truth is explicit and separated from memory, private notes, and agent inferences.
- Corpus pages have cold-readable structure, source citations, status, freshness dates, tags, and links.
- Navigation supports folder, tag, and structural-link traversal.
- Recurring user jobs have retrieval contracts instead of relying only on fuzzy search.
- Audits or evals can detect stale files, unsupported claims, broken links, taxonomy drift, and missing coverage.
- The resulting skill, corpus, or design is domain-neutral unless the user explicitly asked for a domain-specific implementation.
</success_criteria>
