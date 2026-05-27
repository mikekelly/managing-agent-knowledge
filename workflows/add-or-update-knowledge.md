<required_reading>
Read these knowledge files now:

1. `knowledge/writing-patterns.md`
2. `knowledge/source-and-freshness-discipline.md`
3. `knowledge/frontmatter-and-taxonomy.md`
4. `knowledge/navigation-and-links.md`
5. `knowledge/corpus-architecture.md`
</required_reading>

<process>
1. **Classify the change.** Decide whether the work adds a new concept, updates an existing canonical page, creates an index, creates a decision surface, refreshes stale content, or records a known gap.

2. **Read the neighborhood.** Open the nearest index, canonical page, sibling pages, tag taxonomy, and any use-case or bundle that may depend on the change. Do not create a duplicate canonical home.

3. **Inspect sources.** Separate primary authority from secondary commentary and user-provided notes. Verify dates before changing `last_verified`; if verification is incomplete, use a lower status or note the limitation.

4. **Compile, do not dump.** Extract durable rules, examples, exceptions, thresholds, definitions, and decision points. Write the smallest page or edit that gives an agent reusable understanding.

5. **Update metadata.** Set status, freshness date, tags, sources, see-also links, and domain-specific fields. Use only tags from the closed taxonomy unless the task includes adding a new taxonomy term.

6. **Update links.** Add meaningful inline links to canonical homes. Use inclusion links only where the target lives structurally inside the current file's context, usually from indexes or use-case indexes.

7. **Check dependents.** Update sibling pages, synthesis pages, bundles, indexes, changelogs, and eval fixtures when the new fact changes how an agent should retrieve or cite material.

8. **Validate.** Run available linters or checks. If no tooling exists, manually check frontmatter, relative links, source support, tag validity, freshness semantics, and whether the page is readable cold.
</process>

<success_criteria>
This workflow is complete when:

- The corpus has one canonical home for the concept or fact.
- New or changed claims are supported by the right source tier.
- Freshness and status accurately reflect what was verified.
- Links, tags, indexes, and retrieval contracts still guide an agent to the page.
- Any uncovered source gap or uncertainty is made explicit.
</success_criteria>
