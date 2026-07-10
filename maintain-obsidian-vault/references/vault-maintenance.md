# Vault Maintenance Reference

## Cadence

Recommended recurring cycle:

- After every project import: audit links and frontmatter.
- Weekly: review new notes, missing frontmatter, orphan notes, and unresolved links.
- Monthly: review placeholders, duplicate concepts, stale drafts, and indexing exclusions.
- Before RAG ingestion: run full audit, secret scan, and indexing-policy check.

## Obsidian practices encoded by this skill

- Use properties/frontmatter for structured metadata.
- Use internal links and aliases to connect related concepts.
- Use tags for broad filtering, not as a replacement for semantic links.
- Use hub/index pages for navigation across projects and technologies.
- Use database-like review views such as Obsidian Bases when humans need recurring queue review.

## RAG-oriented maintenance

High-quality retrieval depends on:

- stable titles
- explicit status metadata
- source file paths
- heading-aware chunks
- canonical terminology
- exclusion of secrets and generated dependencies
- clear distinction between authoritative notes and placeholders

## Review checklist

For each new or changed Markdown file:

- Does it have frontmatter unless intentionally secret-like/raw?
- Is `title` human-readable and stable?
- Is `type` specific enough?
- Is `status` correct?
- Are aliases used for common synonyms?
- Are links semantic rather than keyword-heavy?
- Does `See also` connect the note to hubs and canonical concepts?
- Are unsupported claims marked as unknown or inferred?
- Should the note be excluded from indexing?

## Cleanup candidates

Flag but do not delete:

- generated app directories
- dependency directories
- build output
- one-off prompts
- duplicate drafts
- stale project exports
- secret-like Markdown files
- notes with unclear status

## Suggested user-facing summary

Report maintenance work in this format:

- Changed: concise file list or categories.
- Added: hubs, placeholders, or reports.
- Skipped: secret-like files and generated artifacts.
- Validation: unresolved wikilinks, missing frontmatter, known risks.
