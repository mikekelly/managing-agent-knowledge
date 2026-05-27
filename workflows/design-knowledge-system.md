<required_reading>
Read these knowledge files now:

1. `knowledge/corpus-architecture.md`
2. `knowledge/writing-patterns.md`
3. `knowledge/frontmatter-and-taxonomy.md`
4. `knowledge/navigation-and-links.md`
5. `knowledge/source-and-freshness-discipline.md`
6. `knowledge/stewardship-and-evals.md`
</required_reading>

<process>
1. **Mine existing context.** Read the user's repo, docs, source files, previous conventions, and example outputs before asking questions. Identify the current implicit corpus rules and repeated agent failure modes.

2. **Define authority boundaries.** Name the canonical sources, secondary sources, user-provided context, private memory, and generated summaries. Specify which surfaces may support final claims and which are hints only.

3. **Choose content layers.** Define the stable doctrinal/reference layer, synthesis or comparison surfaces, frontier/change-tracking pages, history/gaps pages, and use-case/operator pages only where the domain needs them.

4. **Design the file model.** Pick a root such as `knowledge/`, domain or collection subdirectories, section indexes, concept files, source files, use-case files, and synthesis pages. Keep the design predictable enough that an agent can infer parallel paths.

5. **Design metadata.** Define required frontmatter fields, status values, freshness dates, source records, tags, see-also links, and any domain-specific fields such as sections, clauses, product ids, regions, owners, or risk levels.

6. **Design navigation.** Specify the folder taxonomy, closed tag taxonomy, inclusion-link convention, index-page responsibilities, cross-linking style, and rules for asserting corpus silence.

7. **Design retrieval.** Decide which questions are answered by direct file reads, tag lookup, tree traversal, bundles, semantic search, upstream source fetches, or private memory hints.

8. **Design stewardship.** Add health checks, eval prompts, freshness thresholds, link checks, citation checks, and a backlog path for gaps. Decide what the maintainer may fix automatically and what requires human review.

9. **Produce the artifact.** Create or update the conventions, structure, templates, or repo files requested by the user. Keep the design as small as possible while preserving the authority model.
</process>

<success_criteria>
This workflow is complete when:

- The corpus has an explicit purpose, reader, authority hierarchy, and memory boundary.
- File structure, metadata, source discipline, links, tags, and freshness rules are specified.
- The design includes at least one validation path: lint, audit, eval, verifier, or review checklist.
- The user can add the next page or bundle without re-deriving the architecture.
</success_criteria>
