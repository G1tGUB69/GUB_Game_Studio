# Diagram Design — vendored copy

**Original work:** https://github.com/cathrynlavery/diagram-design
**Version:** 2.6.174 (plugin manifest; `SKILL.md` metadata says 2.6)
**License:** MIT (`LICENSE`); bundled icon and font licences in `THIRD_PARTY_LICENSES.md`
**Author:** Cathryn Lavery

## What was copied

| Upstream | Here |
|---|---|
| `skills/diagram-design/` | `.claude/skills/diagram-design/` |
| `commands/doctor.md` | `.claude/commands/diagram-doctor.md` |
| `commands/profile.md` | `.claude/commands/diagram-profile.md` |
| `commands/export-diagram.md`, `commands/import-{drawio,excalidraw,mermaid,plantuml}.md` | `.claude/commands/` (same names) |
| `LICENSE`, `README.md`, `THIRD_PARTY_LICENSES.md`, `CHANGELOG.md` | this folder |

## Local changes

Upstream ships as a plugin, so its commands are namespaced (`/diagram-design:doctor`).
Copied into a project they are not, and `/doctor` and `/profile` were too generic
next to the studio's own skills. So:

- `doctor` → `/diagram-doctor`, `profile` → `/diagram-profile`; the other five keep their names.
- Command files: plain-text paths `skills/diagram-design/…` → `.claude/skills/diagram-design/…`
  (the `../skills/…` Markdown links already resolve from `.claude/commands/`).
- Skill references (`doctor.md`, `export.md`, `export-registry.md`, `import-*.md`):
  `/diagram-design:<cmd>` → the local command name. No other skill content changed.

## Not copied

The repository's maintainer tooling: `scripts/verify-*.py`, `scripts/test-*.py`, CI,
plugin manifests for other hosts, `prompts/` (Codex), screenshots and ADRs. Some
references still name those scripts (e.g. `scripts/verify-motion.py`,
`scripts/verify-contrast.py`, the repository-integrity section of `references/doctor.md`).
They are upstream's own CI checks; they do not exist here, and `/diagram-doctor`
will report them missing. The skill's runtime helpers in
`.claude/skills/diagram-design/scripts/` (`self_check.py`, `verify_geometry.py`,
`export_svg.py`, `export_png.py`, the four `*_extract.py` importers) are all present.

## Requirements

Python 3 for the helper scripts; `playwright` (plus `playwright install chromium`)
for PNG/SVG export. Diagrams themselves are self-contained HTML and need neither.

## Updating

Re-copy `skills/diagram-design/` and `commands/` from upstream, then reapply the
renames above (`grep -rn "diagram-design:" .claude/` should return nothing).
