<overview>
Metadata is the agent control surface. It lets tools filter, freshness checkers warn, verifiers reject weak answers, bundles load the right context, and maintainers find work.
</overview>

<baseline_frontmatter>
Use a small required schema and extend only for domain-specific needs:

```yaml
---
title: Human-readable title
domain: domain-slug
category: section-slug
status: stub | draft | review | stable
last_verified: YYYY-MM-DD
tags:
  - lower-kebab-case
sources:
  - title: Source title
    url: https://example.com/source
    accessed: YYYY-MM-DD
    kind: primary | regulation | guidance | judgment | gov-page | secondary | internal
see_also:
  - ./related-file.md
---
```

Common extensions:

- `as_of` and `expected_decay` for frontier pages.
- `articles_covered`, `sections_covered`, `clauses_covered`, or `source_ids` for source-index pages.
- `persona` and `task` for use-case pages.
- `owner`, `review_cycle_days`, or `risk_level` for enterprise corpora.
- `last_verified_by` when human, agent, and hybrid verification must be distinguished.
</baseline_frontmatter>

<status_semantics>
- `stub`: valid placeholder with metadata and intended scope; not enough for authoritative answers.
- `draft`: substantive content exists but is not fully source-verified.
- `review`: source-checked and awaiting second pass or approval.
- `stable`: source-checked, linked, and considered current as of `last_verified`.

Status must affect agent behavior. A status enum that nobody reads is decorative.
</status_semantics>

<taxonomy_rules>
- Keep tags closed and documented. Agents should not have to guess synonyms.
- Use lower-kebab-case tags.
- Prefer 5-10 tags for substantive pages when the domain is cross-cutting; fewer for small corpora.
- Use tags from multiple dimensions where useful: subject, concept, process, source type, persona, geography, product, risk.
- Add new tags through an explicit taxonomy update, then apply them to obvious existing pages in the same change.
- Treat a zero-result tag lookup as a possible vocabulary gap. Search text before asserting the corpus is silent.
</taxonomy_rules>

<validation>
Validate:

- Required fields exist and parse.
- Dates are ISO `YYYY-MM-DD`.
- Status values are known.
- Tags exist in the taxonomy.
- Source URLs and relative links resolve where tooling permits.
- Domain-specific ids match expected patterns.
</validation>
