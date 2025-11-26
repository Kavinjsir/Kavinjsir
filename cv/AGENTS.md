# Codex Agent Guide: Resume Repository

## Repository Overview
- Primary source: `resume.tex`; class/style helpers in `resume.cls` and `fontawesome*.tex`.
- Custom fonts are vendored under `fonts/`; keep the directory structure intact.
- Build artifacts (`resume.pdf`, `.aux`, `.log`, `.out`) are generated in place by XeLaTeX.

## Editing Workflow
1. Make LaTeX edits in `resume.tex`. For structural tweaks, review `resume.cls` before changing shared macros.
2. Keep entries concise; prefer commented-out alternatives already in the file when restoring past bullets.
3. Preserve ASCII; only introduce new packages or fonts if absolutely necessary.
4. When touching data (dates, roles, links), double-check for consistency across sections.

## Build Instructions
- Compile from the repo root: `xelatex resume.tex`
- Run XeLaTeX twice if references or symbols appear incorrect.
- CI is manual: inspect the CLI output for warnings/errors and open `resume.pdf` to confirm layout.

## Validation Checklist
- No LaTeX warnings about missing fonts or undefined references.
- PDF reflects intended changes and remains single-page unless specifically approved.
- Contact info and URLs render correctly and remain current.

## Housekeeping
- Do not commit transient build files besides the final `resume.pdf` unless asked.
- When updating the PDF, regenerate it immediately after the `.tex` change so they stay in sync.
- Summarize changes for the user, including any layout trade-offs or new dependencies.
