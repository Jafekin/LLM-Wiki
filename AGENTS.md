# Repository Guidelines

## Project Structure & Module Organization

This repository is an Obsidian knowledge vault, not an application codebase. Write curated notes under `wiki/` and keep original materials in `raw/`.

- `wiki/concepts/`: techniques and terminology, such as [[concepts/BM25]].
- `wiki/entities/`: named tools, organizations, people, and datasets.
- `wiki/sources/`: source notes for papers, articles, talks, and books.
- `wiki/queries/`: unresolved research questions.
- `wiki/comparisons/` and `wiki/synthesis/`: side-by-side analysis and cross-source conclusions.
- `wiki/index.md` is the vault directory; `wiki/log.md` records activity in reverse chronological order.
- `schema.md` defines required metadata and page types; `purpose.md` records project scope.

## Authoring & Naming Conventions

Create Markdown files with lowercase `kebab-case.md` slugs where practical (for example, `chain-of-thought.md`); source notes use `author-year-slug.md`. Keep existing Chinese titles and filenames consistent when extending their topic area.

Every page begins with YAML frontmatter containing `type`, `title`, `tags`, `related`, `created`, and `updated` (`YYYY-MM-DD`). Source pages additionally include `authors`, `year`, `url`, and `venue`.

Use Obsidian Flavored Markdown. Reference vault notes with clickable wikilinks, e.g., [[BM25]] or [[concepts/BM25]]. Use `$...$` for inline math and `$$...$$` for display math. Leave one blank line before every Markdown table.

## Content Quality Checks

There is no build system or automated test suite. Before committing, manually check that:

- frontmatter matches the schema and dates are current;
- wikilinks resolve to the intended note;
- new concepts and entities appear in `wiki/index.md` with a one-line description;
- meaningful research activity is logged in `wiki/log.md`;
- claims distinguish source evidence from synthesis, and conflicting evidence is tracked through a query note.

## Commit & Pull Request Guidelines

The existing history uses short operational messages, e.g., `vault backup: 2026-07-14 00:14:11` and `reinitialize repository`. Use concise imperative messages that identify the vault change, such as `add BM25 source notes` or `update RAG synthesis`.

Keep pull requests focused. Include a brief summary, list the notes or sources changed, link any related query or issue, and mention manual link/frontmatter checks. Add screenshots only when a visual Obsidian rendering change needs review.
