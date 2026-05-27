<overview>
An agent knowledge system is a compiled layer between raw sources and runtime answers. It should be shaped for agents that arrive cold, traverse selectively, cite source-backed pages, and hand maintenance work back to an editorial process.
</overview>

<core_layers>
Use only the layers the domain needs, but keep their roles distinct:

- **Canonical reference layer:** stable source-backed concept pages. This is the default authority surface.
- **Synthesis layer:** comparison maps, decision frameworks, cross-domain summaries, and other pages that intentionally span concepts.
- **Frontier layer:** changing or anticipated developments with explicit `as_of`, expected decay, and refresh triggers.
- **History or trajectory layer:** stable retrospectives, milestones, bibliographies, and gap catalogues that explain how the domain reached its current shape.
- **Use-case layer:** persona or operator pages that answer "what do I do?" and link back to canonical concept pages for authority.
- **Procedural layer:** skills, prompts, workflows, and retrieval contracts that tell agents how to use the corpus.
- **Private memory layer:** workspace, user, project, or session-specific facts. This layer can influence retrieval and framing but should not contaminate canonical knowledge.
</core_layers>

<file_model>
Prefer predictable paths and parallel structure:

```text
knowledge/
  index.md
  tags.md
  sources.md
  <domain-or-collection>/
    index.md
    <section>/
      index.md
      <concept>.md
    use-cases/
      <persona>/
        index.md
        <task>.md
    frontier/
    history/
```

Parallel structure matters. If two domains share a concept, mirror paths where practical so agents can infer likely neighbors during comparison.
</file_model>

<design_rules>
- Keep one concept per file unless a decision surface is intentionally cross-cutting.
- Make every concept page readable without its parent index.
- Make every index page explain what the section is, when to use it, where to start, and which children matter.
- Put durable facts in canonical pages and have use-case, synthesis, and bundle surfaces link to them.
- Treat gaps as content. A `gaps.md` or audit page prevents agents from mistaking silence for coverage.
- Treat conventions as part of the system. Agents need operational rules, not only content.
</design_rules>

<anti_patterns>
- Dumping raw PDFs, transcripts, or scraped pages into `knowledge/` without synthesis.
- Treating generated summaries as source-backed canonical pages.
- Mixing workspace-specific examples into shared canonical files.
- Writing a single giant handbook that agents must partially sample.
- Creating many near-duplicate pages because no canonical home was chosen.
- Designing only for human browsing and then expecting agents to retrieve reliably.
</anti_patterns>
