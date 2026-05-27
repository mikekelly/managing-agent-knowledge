<overview>
Corpus tools are part of the knowledge system. Their descriptions, parameters, output envelopes, and errors determine whether agents retrieve the right source and recover from mistakes.
</overview>

<tool_surface_principles>
- Start with simple, direct tools for common paths.
- Keep broad semantic search for vocabulary gaps and long-tail discovery.
- Cap always-loaded tools; use on-demand tools or skills for rare operations.
- Avoid extra invocation layers over code the agent runtime owns. Use MCP, CLIs, or services when there is a real boundary.
- Instrument behavior and specialize from observed misses.
</tool_surface_principles>

<core_tool_set>
Common corpus tools:

- `getFile(path, depth, parentContext)`: read a known page and optionally structural children or parents.
- `getBySourceId(source, id)`: resolve a known section, clause, endpoint, or record to its canonical page.
- `findByTag(tags, mode)`: deterministic closed-taxonomy retrieval.
- `tree(path, depth)`: inspect structural inclusion links.
- `neighbors(path)`: inspect see-also, tags, parents, siblings, and children.
- `freshnessCheck(paths, thresholds)`: compute age and warn/stale verdicts.
- `getBundle(persona, task)`: load a precompiled retrieval contract.
- `semanticSearch(query)`: fuzzy fallback when vocabulary does not map to tags.
- `inventory(section)`: list available files, statuses, and counts.
</core_tool_set>

<description_template>
Write each tool description with five parts:

1. Core purpose in domain terms.
2. When to use it.
3. When not to use it, especially against overlapping tools.
4. Relationships and ordering with sibling tools.
5. Result shape and what the agent should do next.

Descriptions are matching and behavior contracts, not marketing copy.
</description_template>

<output_contract>
Outputs should be compact and actionable:

- Include enough fields for the next decision, not every field by default.
- Return definitive empty states.
- Return structured errors to the agent with stable `error_kind` values.
- Include truncation signals and total counts when output is capped.
- Include `help[]` suggestions with parameterized next-step calls.
- Include status, freshness, and source-tier fields when they affect authority.
- Prefer a readable text format for agent consumption where the harness permits it.
</output_contract>

<error_examples>
Good error shapes:

```yaml
error_kind: unknown_tag
message: "Tag 'privacy-policy' is not in the closed taxonomy."
did_you_mean:
  - privacy
  - policy
help:
  - "Read tags.md before retrying."
```

```yaml
error_kind: file_not_found
path: knowledge/payments/refunds.md
nearest:
  - knowledge/payments/refund-policy.md
  - knowledge/payments/refund-exceptions.md
```
</error_examples>
