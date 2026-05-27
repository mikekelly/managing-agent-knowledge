<overview>
Retrieval contracts are precompiled context packages for recurring jobs. They say what an agent should load, cite, verify, and refuse before answering a known persona-task shape.
</overview>

<when_to_create>
Create a bundle when:

- The same persona or task recurs.
- Correct answers require the same small cluster of files.
- The task has a specific citation pattern or freshness threshold.
- Ad-hoc search repeatedly misses adjacent context.
- The agent wastes turns discovering the same sources.

Do not create a bundle for every possible question. Let ad-hoc retrieval handle the long tail.
</when_to_create>

<bundle_fields>
A useful bundle usually includes:

- `persona`: the role or user type.
- `task`: the operator-shaped job.
- `trigger_description`: plain-English routing signal.
- `required_files`: paths with role and why.
- `required_source_sections`: source ids, clauses, articles, docs, APIs, or records the agent must be able to cite precisely.
- `related_tags`: closed-taxonomy tags to expand.
- `related_bundles`: adjacent tasks for drift.
- `freshness_warn_days` and `freshness_stale_days`.
- `refusal_rules`: statuses, stale verdicts, or missing files that block the bundle.
- `citation_pattern`: required final-answer grounding.
- `session_priming`: one short summary of what the agent should walk in knowing.
</bundle_fields>

<roles_for_required_files>
Use roles to make context selection auditable:

- `canonical-concept`: the authoritative explanation.
- `source-index`: maps source ids, articles, clauses, or endpoints to pages.
- `use-case-anchor`: operator-shaped task page.
- `procedural-context`: how the user acts on the rule.
- `synthesis-context`: comparison or decision surface.
- `frontier-context`: changing development with decay rules.
- `gap-context`: known missing coverage that affects the answer.
</roles_for_required_files>

<routing_tests>
For each bundle, test:

- Obvious trigger: should load the bundle.
- Casual trigger: user uses non-canonical wording but same task.
- Adjacent task: should load a different bundle or no bundle.
- Overlap: two bundles seem plausible; routing should pick the more specific one.
- Stale or missing required file: bundle should refuse, warn, or fall back as designed.
</routing_tests>

<anti_patterns>
- Treating the bundle as a long system prompt.
- Loading two or more bundles by default.
- Listing files without saying why each is required.
- Using invented tags or fuzzy keywords where a closed taxonomy exists.
- Ignoring freshness and status just because a file is in the bundle.
</anti_patterns>
