<required_reading>
Read these knowledge files now:

1. `knowledge/retrieval-contracts-and-bundles.md`
2. `knowledge/frontmatter-and-taxonomy.md`
3. `knowledge/source-and-freshness-discipline.md`
4. `knowledge/navigation-and-links.md`
5. `knowledge/stewardship-and-evals.md`
</required_reading>

<process>
1. **Identify the recurring job.** Define the persona, task, triggering user language, expected answer shape, and why ad-hoc search is not enough.

2. **Find the canonical working set.** Read the use-case page if one exists, the concept pages it depends on, source-index or article pages, relevant synthesis pages, and adjacent sibling pages.

3. **Declare required context.** List required files with role and why, required source sections or article ids, related tags, related bundles, and optional context that should be fetched only if the question drifts.

4. **Set freshness and status gates.** Define warn and stale thresholds, unacceptable statuses, stale-bundle behavior, and whether upstream source fetching is mandatory before answering.

5. **Define citation behavior.** Specify the citation pattern the final answer must follow, including source tier preference and what to do when only secondary support exists.

6. **Write routing signals.** Add a short trigger description, keywords, required terms, negative routing cases, and disambiguation rules when adjacent bundles overlap.

7. **Add session priming.** Summarize what the agent should walk in knowing in one or two paragraphs. Do not turn the bundle into a system prompt; keep it a retrieval contract.

8. **Validate with prompts.** Test at least one obvious trigger, one casual/indirect trigger, one adjacent task that should not route here, and one stale or missing-file case.
</process>

<success_criteria>
This workflow is complete when:

- The bundle identifies persona, task, trigger, required files, required source sections, tags, freshness gates, refusal rules, citation pattern, and related bundles.
- Each required file has a specific role and reason.
- The bundle is small enough to fit the intended context budget.
- Trigger tests show when the bundle should and should not load.
</success_criteria>
