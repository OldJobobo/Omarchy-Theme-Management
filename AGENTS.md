# Repository Guidelines

## Project Structure & Module Organization
This is a documentation-only repository for Omarchy theme management.
- `README.md`: short entry point and link to the main guide.
- `Omarchy-theme-management.md`: canonical technical reference (paths, scripts, switching flow, integrations).
- `AGENTS.md`: contributor instructions for maintaining docs quality.

Keep new files at the repository root unless there is a strong reason to introduce a `docs/` subdirectory.

## Build, Test, and Development Commands
There is no build or runtime in this repo. Validate changes with quick documentation checks:
- `rg --files`: confirm file placement.
- `rg "omarchy-theme-set|omarchy-theme-bg-next|omarchy-hook" Omarchy-theme-management.md`: verify core command references.
- `wc -w README.md AGENTS.md Omarchy-theme-management.md`: monitor doc size and keep edits focused.

If you verify behavior on a live system, mention the command used (for example: `omarchy-theme-current`) in your PR notes.

## Writing Style & Naming Conventions
Use concise, technical Markdown.
- Use clear heading levels (`#`, `##`, `###`) and short sections.
- Put commands and paths in backticks.
- Prefer bullets over long prose for procedures.
- Use lowercase, hyphenated filenames (example: `theme-path-notes.md`).
- Keep terminology consistent with Omarchy script names and file names.

## Validation Guidelines
Treat validation as accuracy review:
- Confirm script names, paths, and behavior descriptions are correct.
- Call out version scope when relevant (example: `Omarchy v3.3.x`).
- Avoid speculation; mark unknowns clearly.

## Commit & Pull Request Guidelines
Use focused docs commits:
- Commit format: `docs: <imperative summary>`.
- One topic per commit.

PRs should include:
- What changed and why.
- Files updated.
- How facts were verified (commands, source scripts, or observed behavior).

## Security & Configuration Notes
Do not commit secrets, tokens, or machine-specific private data. Use `~`-based paths in examples and add caution around destructive commands.
