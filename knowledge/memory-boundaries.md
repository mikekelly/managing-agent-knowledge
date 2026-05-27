<overview>
Knowledge systems fail when canonical facts, private memory, and generated inferences are mixed. Define memory tiers by lifetime, writer, authority, and citation rules.
</overview>

<tiers>
**Working memory:** current context window. Short-lived, agent-managed, not authoritative.

**Episodic memory:** session transcript or task history. Useful for continuity, not a source of truth.

**Semantic/private memory:** workspace, user, team, or project notes. Persistent and agent-writable under rules. Can influence retrieval and framing.

**Procedural memory:** skills, prompts, workflows, and tools. Versioned instructions for how agents work.

**Canonical knowledge:** source-backed corpus pages. Editorially maintained and authoritative within their freshness and status limits.

**Primary sources:** upstream authority. They outrank the compiled corpus when current source text conflicts with the corpus.
</tiers>

<authority_matrix>
For each tier, decide:

- Who can write?
- Who can read?
- How long does it live?
- Can it support a final claim?
- Can it be cited to the user?
- What validates it?
- How is it deleted or superseded?

Document this matrix before building memory tools.
</authority_matrix>

<contamination_controls>
- Do not write workspace-specific facts into a shared corpus.
- Do not promote agent summaries to canonical knowledge without source review.
- Do not let memory override a fresher or higher-tier source.
- Do not cite private memory for high-stakes external facts unless the user explicitly asks for workspace-local context.
- Keep generated eval outputs and conversation logs out of canonical pages except as evidence for a backlog item.
</contamination_controls>

<good_memory_use>
Private memory can safely:

- Remember user preferences.
- Recall matter or project context for retrieval.
- Store house views clearly marked as private or internal.
- Suggest which canonical pages to read.
- Track repeated gaps that should become editorial tasks.

Private memory should not silently become the answer's authority.
</good_memory_use>
