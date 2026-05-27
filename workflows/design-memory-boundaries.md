<required_reading>
Read these knowledge files now:

1. `knowledge/memory-boundaries.md`
2. `knowledge/source-and-freshness-discipline.md`
3. `knowledge/retrieval-contracts-and-bundles.md`
4. `knowledge/stewardship-and-evals.md`
</required_reading>

<process>
1. **Name the tiers.** Define working context, episodic/session history, private semantic memory, procedural skills, canonical knowledge, and external primary sources for the system at hand.

2. **Assign write authority.** Specify which actors can write to each tier: agent, human editor, scheduled maintainer, tenant admin, CI job, or external sync. Default canonical knowledge to human-reviewed writes.

3. **Assign claim authority.** Specify which tiers may support final claims. In high-stakes domains, private memory and generated summaries may shape retrieval and framing but must not be cited as authority.

4. **Define contamination barriers.** Prevent agent conclusions, tenant-specific facts, customer names, private examples, and stale summaries from being written into the shared corpus.

5. **Define retrieval behavior.** Decide when memory hints can alter search, when canonical corpus reads are mandatory, and when a verifier must reject memory-backed claims.

6. **Define forgetting and evolution.** Private notes can evolve, conflict, expire, or be forgotten. Canonical corpus pages are updated by source-backed edits and git history, not by overwriting memory.

7. **Add tests.** Create scenarios where the agent has a tempting memory note that conflicts with the corpus, a stale canonical page, a tenant-specific preference, and a missing source.
</process>

<success_criteria>
This workflow is complete when:

- Every memory tier has a lifetime, writer, reader, and authority level.
- Canonical knowledge cannot be contaminated by agent inference or tenant-private facts.
- Final-claim citation rules explicitly say whether memory can be cited.
- Tests cover conflicts between private memory and canonical sources.
</success_criteria>
