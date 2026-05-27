<overview>
A corpus decays unless maintenance work is visible. Stewardship turns decay, gaps, verifier failures, and search misses into reports, backlog items, patches, and evals.
</overview>

<audit_surfaces>
Regular audits should check:

- Required frontmatter and parseable dates.
- Tags from the closed taxonomy.
- Broken relative links and dead source URLs.
- Stale `last_verified` dates by risk tier.
- Claims without citations.
- Stable pages supported only by weak sources.
- Duplicate or drifting claims across pages.
- Indexes that do not orient cold readers.
- Important pages with no incoming paths.
- Bundles with missing, stale, draft, or stub required files.
</audit_surfaces>

<manager_roles>
If using maintainer agents, keep authority bounded:

- **Auditor:** read-only. Produces reports and backlog items.
- **Refresher:** may fetch upstream sources and propose patches or pull requests. Does not auto-promote high-stakes content to stable.
- **Outreach or reviewer coordinator:** drafts requests for human expert review. Does not send or decide without human approval unless explicitly authorized.
</manager_roles>

<eval_patterns>
Write eval prompts for observed failures:

- Agent answers from prior knowledge without reading the corpus.
- Agent cites a page that does not support the claim.
- Agent misses a relevant sibling or structural parent.
- Agent treats a tag miss as corpus silence.
- Agent relies on stale content without warning.
- Agent routes to the wrong bundle.
- Agent lets private memory override canonical knowledge.
- Agent fails to surface a known gap.
</eval_patterns>

<audit_report_shape>
A useful report leads with findings:

- Severity.
- File or bundle path.
- Evidence.
- User or agent impact.
- Remediation.
- Whether source verification is required.

Summaries come after findings. Do not bury critical authority risks under aggregate metrics.
</audit_report_shape>

<iteration_loop>
1. Observe a failure in agent behavior, audit, or user feedback.
2. Convert it into a focused eval.
3. Patch the corpus, bundle, tool description, or workflow.
4. Run the eval again.
5. Keep the eval if the failure is likely to recur.
</iteration_loop>
