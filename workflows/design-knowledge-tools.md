<required_reading>
Read these knowledge files now:

1. `knowledge/tool-and-output-contracts.md`
2. `knowledge/navigation-and-links.md`
3. `knowledge/frontmatter-and-taxonomy.md`
4. `knowledge/source-and-freshness-discipline.md`
5. `knowledge/retrieval-contracts-and-bundles.md`
</required_reading>

<process>
1. **List retrieval jobs.** Identify the actions agents repeatedly need: read file, find by tag, fetch source section, traverse tree, load bundle, check freshness, inspect neighbors, audit links, or search fuzzily.

2. **Prefer direct primitives.** For common paths, expose low-parameter tools such as `getFile`, `getById`, `findByTag`, `tree`, or `getBundle`. Keep broad search as a fallback, not the primary surface.

3. **Write descriptions as contracts.** For each tool, specify purpose, when to use, when not to use, ordering with sibling tools, result shape, and what the agent should do next.

4. **Define output envelopes.** Include definitive empty states, status or authority fields, truncation hints, structured errors, and `help[]` next-step suggestions with placeholders rather than invented values.

5. **Bound parameters.** Validate paths, tags, status values, depth, dates, and source ids. Return "did you mean" or nearest valid values when possible.

6. **Choose invocation surfaces deliberately.** Use in-process tools for code owned by the agent runtime. Use MCP or a CLI only when there is a real boundary: separate process, language, organization, human shell workflow, or third-party client.

7. **Instrument behavior.** Log tool calls, wrong-tool retries, zero-result searches, stale reads, bundle misses, verifier rejects, and high-latency paths. Use logs to improve tools and bundles.
</process>

<success_criteria>
This workflow is complete when:

- Each tool maps to a recurring retrieval or stewardship job.
- Tool descriptions make wrong-tool calls less likely.
- Outputs are compact, actionable, and unambiguous on empty or error states.
- The design avoids extra invocation layers over code the runtime already owns.
</success_criteria>
