<required_reading>
Read these knowledge files now:

1. `knowledge/source-and-freshness-discipline.md`
2. `knowledge/frontmatter-and-taxonomy.md`
3. `knowledge/navigation-and-links.md`
4. `knowledge/stewardship-and-evals.md`
5. `knowledge/retrieval-contracts-and-bundles.md`
</required_reading>

<process>
1. **Set audit scope.** Identify the corpus root, target domain, sections, status levels, freshness thresholds, and whether the audit should produce a report only or also patch low-risk defects.

2. **Run mechanical checks.** Check required frontmatter, date formats, tag validity, source record shape, relative links, inclusion-link resolution, duplicate filenames, and unreachable top-level pages.

3. **Check freshness.** Compare `last_verified` or equivalent dates against thresholds. For stale high-impact pages, identify source URLs that need upstream re-checking before any authoritative update.

4. **Check source coverage.** Sample or scan claims for citations. Prioritize pages marked stable, pages used by bundles, pages with high traffic, and pages whose source kind is secondary or unknown.

5. **Check graph health.** Look for index pages that are only flat lists, concept files with no incoming paths, over-tagged or under-tagged files, invented tags, dead see-also links, and structural links under excluded sections.

6. **Check drift and duplication.** Search for repeated claims across pages. If wording differs, identify the canonical home and propose which pages should link instead of restating.

7. **Check retrieval contracts.** For each bundle or persona-task contract, verify required files exist, statuses are acceptable, freshness windows are coherent, related tags are valid, and citation patterns can be enforced.

8. **Write findings first.** Produce findings ordered by severity with file paths, line references when available, impact, and concrete remediation. Separate mechanical fixes from source-dependent editorial work.

9. **Create or update evals.** Add realistic prompts that would have exposed the issue: stale claim, unsupported answer, wrong tag lookup, missing bundle, duplicate rule, or false corpus silence.
</process>

<success_criteria>
This workflow is complete when:

- The audit report distinguishes critical authority risks from hygiene issues.
- Every finding has a reproducible path, impact, and next action.
- Source-dependent changes are not silently made without source verification.
- New or updated evals cover at least the highest-risk failure modes found.
</success_criteria>
