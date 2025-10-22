# Repository Guidelines

This diary repository stores daily reflections in Markdown. Follow the practices below to keep entries consistent, traceable, and easy to surface in the weekly and top-level summaries.

## Project Structure & Module Organization
- Root-level dated files such as `2025_09_29.md` capture historic logs before the `entries` directory migration; leave them untouched unless correcting typos.
- Current daily entries live in `entries/<year>/YYYY-MM-DD.md`; browse `entries/2025/` for the latest examples.
- `template.md` defines the canonical section headings; copy it when drafting a new day.
- `weekly.md` aggregates recent links, while `README.md` pulls the newest entry via the `<!-- LAST_ENTRY_LINK -->` marker—never remove or rename that placeholder.

## Build, Test, and Development Commands
- `ls entries/2025` — confirm placement of a new file before committing.
- `rg "## " entries/2025/2025-10-09.md` — spot-check section coverage or locate headings in similar entries.
- `markdownlint "**/*.md"` — optional but recommended to catch spacing or heading issues if you have the tool installed locally.

## Coding Style & Naming Conventions
- Name new diary files `entries/YYYY/YYYY-MM-DD.md` (zero-padded month and day). Match branch names and PR titles to this pattern, e.g., `2025-10-10.diary`.
- Keep headings from `template.md` in Japanese (`## やったこと`, etc.) and supply concise bullet lists or short paragraphs beneath each.
- Record durations with lowercase units (`2hour`, `30min`), stick to `-` for unordered lists, and keep spacing consistent with recent entries.

## Testing Guidelines
- No automated test suite exists; proofread entries, verify Markdown links (especially weekly summaries), and preview the rendered page if possible.
- Before opening a pull request, ensure any linting you run locally (e.g., `markdownlint`) passes and `git diff` only shows intentional content changes.

## Commit & Pull Request Guidelines
- Follow the existing history: daily entry commits use the message `YYYY-MM-DD.diary`; ancillary updates (e.g., README refresh) can use `chore: update weekly & README`.
- Group related updates together—entry content, `weekly.md`, and `README.md` marker adjustments should land in the same branch/PR.
- PR descriptions should summarise the new reflections, mention the updated files, and link to the rendered entry if previews are available.
