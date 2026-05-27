<overview>
Agent navigation should not depend on one mechanism. Use folders for editorial location, tags for topical retrieval, and structural links for context.
</overview>

<three_axes>
**Folders:** show where content belongs physically. They help editors and make parallel domains predictable.

**Tags:** show what a page is about. They let agents find related material across folders.

**Inclusion links:** show structural parent-child context. A markdown link on its own line, usually in an index, declares that the target lives inside the current file's context.
</three_axes>

<inclusion_link_rule>
A markdown link on its own line is structural:

```markdown
### [Onboarding](./onboarding/index.md)

- [Approval workflow](./approval-workflow.md) - when a request needs review before completion.
```

A markdown link inside prose is a cross-reference:

```markdown
The decision depends on the [approval workflow](./approval-workflow.md) and the current operating policy.
```

Use inclusion links mainly in index pages, persona indexes, source indexes, and decision maps. Concept files usually use inline links and optional related lists.
</inclusion_link_rule>

<exceptions>
Do not treat these bare-line links as structural children:

- Bibliography, sources, references, or further-reading sections.
- See-also, related, cross-reference, or meta sections.
- Markdown reference definitions such as `[source]: https://example.com`.
- External URLs and pure anchor links.
</exceptions>

<retrieval_discipline>
When answering from a corpus:

1. Start from a known bundle, index, tag, or path.
2. Read whole concept files rather than snippets; the file is the retrieval unit.
3. For broad questions, traverse the inclusion-link tree from the relevant index.
4. For a concept file, inspect its structural parent and siblings when the question is multi-part.
5. Use text search before asserting the corpus is silent.
6. Surface silence explicitly when both tag and text search fail.
</retrieval_discipline>

<graph_health>
Watch for:

- Important concept files with no incoming index path.
- Index pages that list files without descriptions.
- Concept files that use bare-line links accidentally.
- Tags that duplicate folder structure without adding topical value.
- Synthesis pages that do not link their underlying canonical pages.
</graph_health>
