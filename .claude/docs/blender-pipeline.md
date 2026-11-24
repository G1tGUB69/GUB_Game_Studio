# Blender Pipeline (blender-* skills)

The 28 `blender-*` skills in `.claude/skills/` are vendored from
**blender-agent-skills v1.3.2** (EL4CTEO, MIT — license at
`.claude/docs/third-party/blender-skills-LICENSE`). They drive Blender 5.2 LTS+
(verified on 5.3) from bpy scripts, either live through a blender-mcp server or
headless from the shell.

They are a **tool pack, not studio workflow skills**: they have no phases,
verdicts or "May I write" steps, and they are not in `studio-tests/catalog.yaml`.
`/skill-test static all` will report them as non-compliant with the studio
rubric — that is expected; judge them against their own source repo instead.

## Entry point

Start every Blender task with `blender-core` — it routes to the specialised
skill and defines how code runs. Finish every geometry task with
`blender-asset-qa` (numbers + a review sheet). End-to-end playbooks (prop,
character, environment, web asset) are in `blender-workflow-recipes`.

In the skills, `<skills_dir>` means `.claude/skills` in this project:

```
python .claude/skills/blender-core/scripts/run_in_blender.py --blend in.blend .claude/skills/blender-asset-qa/scripts/qa_check.py -- --objects Chair
```

Run the scripts; don't read them. Each documents its flags in its docstring and
prints one JSON result.

## Requirements

- **Blender 5.2 LTS or newer.** Found via `$BLENDER_EXE`, then PATH, then the
  standard install folders.
- **Host Python 3.9+** for `run_in_blender.py` (no bpy needed on the host). The
  Windows Store `python` stub does not count — install a real Python.
- Windows + Git Bash: prefix with `MSYS_NO_PATHCONV=1` when a path starts with
  `//`, or run from PowerShell.

## Who uses them

| Studio role | Blender skills |
|---|---|
| `technical-artist` | `blender-asset-qa`, `blender-game-optimization`, `blender-export-pipelines`, `blender-retopology-uv`, `blender-texture-baking`, `blender-pipeline-automation`, `blender-scene-setup` |
| `art-director` (direction only) | sets style for `blender-stylized-npr`, `blender-pbr-materials`, `blender-time-of-day` — never runs them |
| `/asset-spec` output | the per-asset spec is the input to a `blender-workflow-recipes` playbook |
| `/asset-audit` | `blender-asset-qa` and `blender-game-optimization` give the numbers for 3D assets |

Aesthetic choices (palette, style, silhouette) stay with `art-director` and the
art bible; Blender skills implement them.

## Export target by engine

Resolve `engine.name` from `project.yaml`, then use the matching preset in
`blender-export-pipelines`:

| `engine.name` | Format | Reference |
|---|---|---|
| Godot | GLB (glTF binary) | `blender-export-pipelines/references/godot-web.md` |
| Web | GLB, meshopt/Draco, WebP textures | `blender-export-pipelines/references/godot-web.md` |
| Unity | FBX (Humanoid for characters) | `blender-export-pipelines/references/unity.md` |
| Unreal | FBX (skeletal, Nanite, UCX collision) | `blender-export-pipelines/references/unreal.md` |

Exported files go under `assets/` and follow the naming rules the project's
`/asset-audit` checks. Source `.blend` files go beside them or under
`assets/source/` — decide once and record it in the art bible.

## Updating the pack

The skills are a plain copy. To update to a newer release:

1. Copy the new release's `skills/blender-*` folders over `.claude/skills/blender-*`.
2. Replace `.claude/docs/third-party/blender-skills-LICENSE` with its `LICENSE`.
3. Update the version line at the top of this file.

Do not edit the `_bpyx.py` copies by hand: upstream keeps one source
(`shared/_bpyx.py`) and syncs it into every `scripts/` folder.
