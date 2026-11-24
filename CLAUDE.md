# Claude Code Game Studios -- Game Studio Agent Architecture

Indie game development managed through 54 coordinated Claude Code subagents
(49 studio agents + 5 `impeccable-*` design agents).
Each agent owns a specific domain, enforcing separation of concerns and quality.

## Technology Stack

- **Engine**: [CHOOSE: Web / Godot 4 / Unity / Unreal Engine 5]
- **Language**: [CHOOSE: TypeScript / GDScript / C# / C++ / Blueprint]
- **Version Control**: Git with trunk-based development
- **Build System**: [SPECIFY after choosing engine]
- **Asset Pipeline**: [SPECIFY after choosing engine]

> **Note**: Engine-specialist agents exist for Godot, Unity, and Unreal with
> dedicated sub-specialists. Use the set matching your engine.

## Project Structure

@.claude/docs/directory-structure.md

## Blender Asset Pipeline

28 `blender-*` skills (Blender 5.2 LTS+) live in `.claude/skills/`, merged from
blender-agent-skills (MIT, see `docs/third-party/blender-skills/`). Start any
Blender task with the `blender-core` skill; it routes to the right specialist
skill and finishes with `blender-asset-qa`. Read `.claude/docs/blender-pipeline.md`
on demand for the role split and the engine-to-format table.

## Impeccable UI Design

The `impeccable` skill (v0.1.27) and its 5 `impeccable-*` agents live in
`.claude/skills/impeccable/` and `.claude/agents/`, copied from Impeccable
(Apache-2.0, see `docs/third-party/impeccable/`). Use it to design, critique,
audit or polish frontend UI — menus, HUDs, web game shells, DESIGN.md. Its
automatic design-check hooks are intentionally **not** installed; run the skill
on demand.

## Diagram Design

The `diagram-design` skill (v2.6) lives in `.claude/skills/diagram-design/`, with
7 slash commands in `.claude/commands/`, copied from Diagram Design (MIT, see
`docs/third-party/diagram-design/`). Use it for editorial HTML/SVG diagrams —
architecture, flowcharts, state machines, system dependency maps, timelines,
Gantt, charts — e.g. for ADRs, GDD system maps and milestone docs.
`/import-mermaid|drawio|excalidraw|plantuml` redraw existing diagrams,
`/export-diagram` writes SVG/PNG (needs Python + Playwright), and
`/diagram-doctor` / `/diagram-profile` are its renamed `doctor` / `profile`.
Its first run asks to set a style guide; keep that in line with the art bible.

## Engine Version Reference

<!-- ENGINE-REFERENCE-IMPORT: the line under this comment is engine-specific,
     and there is none until an engine is set. /setup-engine, the grow's record
     step and /project-settings (engine.name) write
     @docs/engine-reference/<engine>/VERSION.md here for the chosen engine. Skills
     that need the pinned version read that file on demand either way. -->


## Technical Preferences

`project.yaml` at the repo root is the primary config store — engine, specialists,
naming, platform, performance, modes. Skills resolve it via `resolve_config`
(see `.claude/docs/config-resolution.md`).

`.claude/docs/technical-preferences.md` is the **legacy fallback**, read on demand
when a key is absent from `project.yaml`. It is not imported here: before
`/setup-engine` runs it is almost entirely `[TO BE CONFIGURED]` placeholders, and
after it runs `project.yaml` holds the real values.

## Coordination Rules

@.claude/docs/coordination-rules.md

## Collaboration Protocol

**User-driven collaboration, not autonomous execution.**
Every task follows: **Question -> Options -> Decision -> Draft -> Approval**

- Agents MUST ask "May I write this to [filepath]?" before using Write/Edit tools
  (exempt: `active.md` appends, agent memory, a subagent's new file at the path
  its orchestrating skill named; see `.claude/rules/agent-memory.md`)
- Agents MUST show drafts or summaries before requesting approval
- Multi-file changes require explicit approval for the full changeset
- No commits without user instruction
- A skipped or dismissed question is not an answer: act on nothing, re-ask in
  plain text and wait
- Started outside this file's folder? Warn first: hooks, deny rules and the
  ask-first mode load only when Claude Code starts here

See `docs/COLLABORATIVE-DESIGN-PRINCIPLE.md` for full protocol and examples.

> **First session?** Say "make me a game" (`/prototype`), or run `/start` to begin
> the guided onboarding flow.

## Coding Standards

@.claude/docs/coding-standards.md

## Context Management

Read `.claude/docs/context-management.md` on demand — it is a reference, not
session context. Two of its conventions are load-bearing and cited by name
elsewhere in the repo, so they are restated here rather than lost:

- **`production/session-state/active.md` is the session checkpoint.** The file is
  the memory, not the conversation. Read it first after any compaction, crash, or
  `/clear`.
- **Helpers in `.claude/scripts/` emit observations, never verdicts.** A script
  that scores or judges will eventually contradict a mode or override it cannot
  see. (Cited by `artifact-check.sh` and `adr-dep-graph.sh`.)
