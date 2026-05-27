<overview>
An agent knowledge corpus earns reliability by saying where claims came from, when they were checked, and what the agent must do when material is stale, weakly sourced, or missing.
</overview>

<source_hierarchy>
Define a domain-specific hierarchy. A generic pattern:

1. Primary source of truth: signed policy, contract, code, database row, official record, source repository, published API spec, or maintained source document.
2. Authoritative interpretation: official guidance, formal decision, internal approved interpretation, or implementation note.
3. Operational guidance: approved runbook, standard operating procedure, maintained playbook.
4. Reputable secondary source: analyst note, vendor guide, implementation guide, external commentary.
5. User-provided or agent-generated context: useful for framing, not authority unless separately verified.

Agents should prefer the highest available tier and flag when only lower-tier support exists.
</source_hierarchy>

<freshness_contract>
`last_verified` means the page was checked against the relevant source on that date. It is not a modification timestamp. Do not bump it when only wording changes unless the source was actually checked.

Typical behavior:

- Fresh: answer normally.
- Warn: cite but tell the user the file is aging and may need source re-check.
- Stale: do not rely on the corpus page alone for authoritative claims. Fetch or inspect the upstream source, refuse, or caveat depending on the domain.

Thresholds should vary by risk. A security, pricing, compliance-change, or incident-response page may decay in days. A stable historical explainer may decay in years.
</freshness_contract>

<citation_rules>
- Every high-impact claim should attach a source or corpus citation.
- A citation must support the claim actually made, not merely point to a related page.
- If the corpus is silent, say so. Do not fill gaps from parametric model knowledge.
- If a secondary source is the only support, label it as secondary where the user might over-rely.
- If sources conflict, cite the conflict and explain which source tier controls.
</citation_rules>

<update_rules>
- Meaning-changing edits require source review, freshness review, and dependent-page review.
- If verification is partial, lower the status or add an explicit limitation.
- When a source changes, update the canonical page in place and let git preserve history.
- When a user or agent finds an error, create a correction task that names the source to check.
</update_rules>
