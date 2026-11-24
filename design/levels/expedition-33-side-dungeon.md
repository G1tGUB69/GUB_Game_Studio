# Level Design Brief: Optional Side Dungeon
## Clair Obscur: Expedition 33 -- External Level Design Commission

**Status:** DRAFT for Sandfall review. Not yet cleared to send.
**Audience:** External freelance level designer.
**Author role:** Level design (drafted for Sandfall Interactive).

**How to read this brief.**
- `[SANDFALL TO PROVIDE: ...]` marks information only the studio owns. Do not guess it. Ask, or wait for the supplied value.
- `PROPOSAL` marks a suggestion that needs Sandfall approval before it is treated as fixed.
- Nothing in this brief is canon unless Sandfall confirms it. Do not invent named characters, factions, lore, enemy types or exact stats. Use neutral working names (for example "Boss A", "Zone 2 Hub") in your documents.

Publicly known traits of the game that this brief relies on:
- Turn-based RPG combat with real-time dodge, parry and counter inputs.
- Third-person exploration of a dark-fantasy, Belle Epoque-inspired world.
- Enemies are visible in the world and engaged by the player.
- Built in Unreal Engine 5.

---

## 1. Purpose & Scope

**What you are making.** One optional side dungeon: a self-contained, hand-authored space the player may choose to enter. It is not required to finish the main story.

**Why it exists.**
- It rewards curious players with a memorable space, a meaningful reward and a small story moment.
- It shows the game's combat and exploration at their best in a compact format.

**In scope**
- Paper design: layout, flow, encounters, pacing, narrative beats, reward placement.
- Engine greybox (blockout only) built to Sandfall's metrics.
- Documentation sufficient for Sandfall's art, audio, narrative and gameplay teams to take over.

**Out of scope**
- Final art, lighting, VFX, audio, cinematics, writing and dialogue.
- New enemy design, new mechanics, new systems, new items or stats.
- Balance values. You propose encounter intent. Sandfall sets numbers.

**What success looks like**
1. A first-time player can enter, explore, fight, and leave without a guide, and never feels lost or cheated.
2. Every combat space can be read at a glance for dodging and parrying.
3. A completionist finds the secrets through observation, not luck or brute force.
4. A player who skips most of the optional branches still has a complete, satisfying run.
5. Sandfall can build the final level from your greybox without redesigning the layout.
6. The dungeon feels like it belongs to this game, not to a generic RPG.

---

## 2. Game & Player Context

Assume the player arrives mid-game, having chosen to detour from the main path. Treat the values below as Sandfall's to fill in.

| Item | Value |
|---|---|
| Story position at entry (earliest point the dungeon unlocks) | [SANDFALL TO PROVIDE: story milestone or world-map region when the entrance becomes available] |
| Recommended player level range | [SANDFALL TO PROVIDE: level range, and whether the dungeon scales to the player] |
| Party size and composition at entry | [SANDFALL TO PROVIDE: number of party members available; which characters may be absent] |
| Skills and abilities unlocked at entry | [SANDFALL TO PROVIDE: list of combat skills, exploration/traversal abilities, and field abilities the player is guaranteed to have] |
| Healing and consumable economy at entry | [SANDFALL TO PROVIDE: typical consumable stock, how healing and resource restoration work outside combat, whether rest points restore everything] |
| Death and retry rules | [SANDFALL TO PROVIDE: what happens on defeat; where the player respawns; what is lost] |
| Expected player skill | [SANDFALL TO PROVIDE: target audience skill level for this content, e.g. "players comfortable with parry timing"] |

**Design assumption until Sandfall says otherwise:** the player can already dodge, parry and counter competently and understands visible-enemy engagement. The dungeon must not teach those basics. It may test them and may introduce one twist at a time.

**Traversal assumption:** only the traversal abilities listed in the table above exist. If an ability is not listed, do not gate content behind it.

---

## 3. Design Pillars for This Dungeon

These are proposed pillars for this dungeon only (PROPOSAL). Sandfall may replace them with the game's official pillars. If official pillars exist, the dungeon pillars must serve them.
[SANDFALL TO PROVIDE: the game's official design pillars, so the freelancer can check alignment]

**Pillar 1: Curiosity pays.**
Looking carefully always beats rushing. Every optional branch ends in something worth the detour. Clues are visible before the secret is reachable.
- Test: for each branch, can you state in one sentence what the player gains?

**Pillar 2: Readable danger.**
Combat is decided by reading telegraphs, not by fighting the camera or the room. Arenas, sightlines and cover never obscure an enemy's attack.
- Test: could a player fail a parry or dodge because of geometry rather than timing? If yes, change the geometry.

**Pillar 3: Melancholic beauty.**
The place is lovely and sad. Quiet moments are as important as fights. The space tells a story of loss or absence through its arrangement.
- Test: remove all text and dialogue. Does a player still sense what happened here?

**Pillar 4: Respect the player's time.**
The dungeon is optional, so it must not waste time. No padding, no backtracking mazes, no unavoidable repeated gauntlets after a defeat.
- Test: after a defeat, how long until the player is fighting the same encounter again? Keep this short (see Section 6).

**Pillar priority when they conflict:** Readable danger > Respect the player's time > Curiosity pays > Melancholic beauty. [SANDFALL TO PROVIDE: confirm or change this ordering]

---

## 4. Narrative & Tone Brief

Narrative decisions belong to Sandfall's narrative team. You provide spatial storytelling and beat placement, not plot.

### 4.1 Premise seed (PROPOSAL, requires Sandfall approval)

> A place the world has quietly forgotten: a grand space that was built for a purpose that has since been lost, and has been left to decay in silence. Whoever made it intended it to preserve something. What remains is a trail of small human traces that lead the player, step by step, to the reason it was abandoned. The final discovery recontextualises everything the player walked past.

This seed deliberately names no characters, factions or lore. Sandfall will replace or approve it.
[SANDFALL TO PROVIDE: approved premise, or a replacement; confirm whether the dungeon connects to main-story lore, party-member arcs, or stands alone]

### 4.2 Emotional arc

| Phase | Target feeling | Spatial tools |
|---|---|---|
| **Enter** | Curiosity, a small unease, awe at scale | Clear threshold, a wide establishing view, one early quiet detail that raises a question |
| **During** | Growing understanding, tension broken by stillness | Traces that accumulate, a mid-point revelation, a quiet space before the climax |
| **Leave** | Bittersweet resolution, a sense of having witnessed something | A calm exit route, a reflective view back, a visible change in the space after the finale |

### 4.3 Environmental storytelling guidelines

1. **Show a before and an after.** Arrange props so a player can infer a prior moment (a table set for people who never returned, a scene interrupted).
2. **One idea per room.** Each space carries at most one story fragment, readable within a few seconds.
3. **Escalate by accumulation.** Early traces are ambiguous. Later traces make the earlier ones make sense.
4. **No text dependency.** Any written or spoken lore is a bonus layer, never required to understand where to go or what to do.
5. **Place story beats away from combat.** Fragments sit in rest spaces and corridors, not in arenas where the player is focused on dodging.
6. **Optional branches hold deeper fragments.** The critical path gives the complete outline. Branches add emotional detail.
7. **Do not add dialogue or text.** Flag where text, audio logs or a cinematic would help, using a marker in your documents. Sandfall decides.
8. **Respect tone.** Melancholic, restrained, never jokey. Avoid shock for its own sake.

[SANDFALL TO PROVIDE: tone guardrails (content limits, themes to avoid), and the narrative contact who approves story beat placement]

---

## 5. Visual & Atmosphere Direction

Art direction is Sandfall's. Your greybox must support it, not pre-empt it.

**Mood:** beautiful, hushed, a little sorrowful. The place looks like it was once cared for.
[SANDFALL TO PROVIDE: art bible, or the sections relevant to environments, palette, materials, and references; confirm which are shareable under the NDA]
[SANDFALL TO PROVIDE: the biome or environmental theme for this dungeon, or confirmation that the freelancer proposes one for approval]

### 5.1 Lighting guidance (intent only)

- Light is the main wayfinding tool. The critical path is the brightest or warmest readable route. Dead ends and secrets are quieter.
- Plan a clear light hierarchy per room: one focal light, secondary fill, dark edges.
- Combat arenas are evenly readable. No pitch-dark corners where an enemy or telegraph can hide.
- Mark light sources in the greybox (placeholder light actors named per Section 10) so lighting artists inherit your intent.
- [SANDFALL TO PROVIDE: lighting rules or limits, e.g. maximum dynamic lights per space, if any]

### 5.2 Shape language

- Use consistent, deliberate shapes so spaces feel authored. Propose one dominant shape logic (for example: grand arches and symmetry that is later broken by collapse) and state it in your paper design.
- Large, simple forms for the critical path. Smaller, more intricate forms for secrets.
- Verticality is welcome if it supports sightlines and orientation, and the metrics allow it.
- Shape language should communicate function: where to walk, what is climbable or interactive, what is dangerous.

### 5.3 Landmarks and wayfinding

- Every zone has at least one **landmark** visible from its entry point and from at least one other zone.
- The **destination** (the next goal) is glimpsed before it is reachable, so the player forms a goal first and works out the route second.
- Use leading lines, light, contrast, and repeating motifs to guide. Avoid UI markers as a crutch.
- Mark each landmark and each leading element on the layout diagram.
- Test: a player who pauses for five seconds in any space should know where to go next.

[SANDFALL TO PROVIDE: wayfinding conventions used elsewhere in the game (e.g. how interactables, climbable surfaces, breakable objects and the critical path are signposted) so the dungeon is consistent]

---

## 6. Structure Requirements

| Item | Requirement |
|---|---|
| Target playtime, critical path only | [SANDFALL TO PROVIDE: target minutes. If undecided, the freelancer proposes a range for approval.] |
| Target playtime, full completion | [SANDFALL TO PROVIDE: target minutes] |
| Number of zones | PROPOSAL: 3 to 4 distinct zones. [SANDFALL TO PROVIDE: confirm or change] |
| Critical path | One clear mandatory route from entrance to final boss, no required backtracking beyond shortcuts |
| Optional branches | PROPOSAL: 2 to 4 branches, each reconnecting to the critical path or ending in a dead end that pays off |
| Secrets | PROPOSAL: 2 to 4 secrets total. [SANDFALL TO PROVIDE: confirm count and what counts as a secret] |
| Shortcuts | At least 1 shortcut that links a late area back to an early one, unlockable from the far side |
| Checkpoints / rest spots | At least one in each zone, plus one before each boss. [SANDFALL TO PROVIDE: how rest spots work in this game and any limits] |
| Entry connection | [SANDFALL TO PROVIDE: world map location, the entrance's physical form, load/transition behavior, and which direction the player arrives from] |
| Exit connection | [SANDFALL TO PROVIDE: where the player appears on leaving; whether the final boss opens a direct route out] |

### 6.1 Structural rules

1. **Loop, don't maze.** Prefer loops and shortcuts to long dead-end corridors.
2. **Zones are distinct.** Each zone has its own identity (shape, lighting, role in the story) and its own landmark.
3. **Hub-and-spoke is allowed** for optional branches only if the hub is a rest spot.
4. **Retry cost is low.** After a defeat the player should reach the failed encounter again without repeating earlier fights. Put checkpoints accordingly. (Pillar 4)
5. **Bosses are not gated by optional content.** The critical path is always completable without any secret.
6. **Optional branches are labelled by the space**, not by a map icon. A branch is visibly a detour.
7. **Exit is easy.** Once the final boss is beaten, leaving must be fast.
8. **Point of no return.** If any exists, it is clearly signalled before the player crosses it. [SANDFALL TO PROVIDE: whether the game allows a point of no return in optional dungeons]

---

## 7. Pacing Curve Template

Pacing is built from tension and rest. Intensity is on a 1 to 5 scale (1 = calm, 5 = peak). The numbers below are ranges for you to adapt, not fixed counts. Sandfall confirms before greybox v1.

[SANDFALL TO PROVIDE: any studio-standard pacing targets or encounter-density benchmarks from existing dungeons that this one should match]

### 7.1 Template (adapt per zone)

```
Intensity
  5 |                                                   *** Final boss
  4 |                  ** Mini-boss            ***
  3 |        ***  *          *   ***   **  *
  2 |   **  *       *  ___  *      *    ___  *
  1 |__*______________/   \_/________/   \______ Exit
     Enter  Zone 1     Zone 2        Zone 3   Boss  Leave
```

Read this as a shape, not a schedule: rise, release, higher rise, release, climax, long exhale.

### 7.2 Beat structure

| Beat | Purpose | Intensity |
|---|---|---|
| Threshold | Establish mood and scale | 1 |
| Early encounter | Remind the player of the rules in a forgiving space | 2 |
| Exploration stretch | Breathing room, first story trace | 1 to 2 |
| Zone 1 challenge | Introduce the dungeon's combat flavor | 3 |
| Rest spot | Recover, read the environment | 1 |
| Zone 2 escalation | Combine a familiar threat with a new arena constraint | 3 to 4 |
| Mini-boss | Mid-point test and revelation | 4 |
| Quiet space | Emotional beat before the next rise | 1 |
| Zone 3 and onward | Highest pressure on the critical path | 3 to 4 |
| Pre-boss rest | Last chance to prepare, signalled clearly | 1 |
| Final boss | Climax | 5 |
| Resolution and exit | Reflection, reward, calm | 1 |

### 7.3 Encounter count guidance (ranges, PROPOSAL)

| Category | Range (critical path) | Range (optional content) |
|---|---|---|
| Standard encounters per zone | 2 to 4 | 1 to 2 per branch |
| Mini-bosses | 1 (mid-dungeon slot) | 0 to 1 optional, only if Sandfall approves |
| Final boss | 1 (end slot) | none |
| Total standard encounters | [SANDFALL TO PROVIDE: confirm overall cap] | |

**Rules**
- Never place two high-intensity beats back to back without a rest spot or a clear calm stretch between them.
- The longest calm stretch sits directly before the final boss.
- Optional branches may spike higher than the critical path only if they are clearly signalled and skippable.
- Boss slots and rules (mini-boss and final boss): you design the arena, approach, rest spot and sightlines. Sandfall supplies the boss. [SANDFALL TO PROVIDE: boss assignments, or confirmation that bosses are designed in-house, plus any arena size or phase requirements]

---

## 8. Encounter & Combat Design Guidelines

The combat system is turn-based with real-time dodge, parry and counter inputs. Your spaces must support reading enemy telegraphs.

### 8.1 What you may and may not decide

| You MAY decide | Sandfall decides (supplied) | You MAY NOT |
|---|---|---|
| Encounter position and spacing | Enemy roster available to this dungeon | Invent enemies, abilities or stats |
| Which supplied enemy types appear where | Exact enemy stats and damage values | Set difficulty numbers |
| Arena shape, size within metrics, cover, sightlines | Enemy AI and behavior | Specify AI code. Describe patrols and pressure zones in plain level terms |
| Patrol routes, sight cones, aggro zones (as intent) | Reward values and drop tables | Change combat rules or input timing |
| Encounter ordering and ramp | Boss designs | Add new mechanics or systems |
| Pacing of rests and checkpoints | Story content | Write lore or dialogue |

[SANDFALL TO PROVIDE: enemy roster for this dungeon, with for each enemy: working name, role, attack telegraph style, approximate size category (not exact), ranged or melee, and any arena restrictions]
[SANDFALL TO PROVIDE: list of enemy types or behaviors that must never be combined in one encounter]
[SANDFALL TO PROVIDE: whether the dungeon uses a dedicated enemy set or reuses overworld enemies, and any level-scaling rules]

### 8.2 Arena readability for dodge and parry

1. **Clear camera.** Keep ceilings high enough and walls far enough that the third-person camera never clips or obscures the player or the attacker during an encounter. [SANDFALL TO PROVIDE: minimum arena dimensions and ceiling height that keep the camera clean]
2. **Visible attackers.** Every enemy is visible during its attack. No pillar, prop or foliage that can hide a wind-up.
3. **Contrast.** Floor, enemy and projectile should read against each other. Flag any space where lighting or materials could undermine that.
4. **Flat and stable fighting surface.** Avoid slopes, clutter and level changes in the combat footprint. The player is not fighting the terrain.
5. **Limited hazards.** Environmental hazards in arenas are allowed only if they are telegraphed, static or slow, and never overlap with an enemy attack window.
6. **No camera-fighting geometry.** Avoid narrow corridors for multi-enemy fights.
7. **Clean boundaries.** The edge of the combat space is obvious. No invisible walls the player discovers by bumping into them.
8. **Props are decoration, not obstacles.** Anything inside the arena footprint must not block movement or vision during a fight.

### 8.3 Enemy placement rules

1. **Enemies are visible before engagement.** The player sees an enemy group from a distance and chooses how to approach. No spawn-behind-the-player, no pop-in on the critical path.
2. **Approach space.** Leave a readable approach zone before each encounter so the player can plan.
3. **Fair first strike.** Where the game lets the player gain an advantage by approaching smartly, the layout should make that possible (a route that allows a flanking approach, for instance). [SANDFALL TO PROVIDE: how first-strike and ambush mechanics work in the overworld so encounters can be placed accordingly]
4. **Patrols are legible.** Patrol routes are short, loop-based and visible from at least one safe vantage point.
5. **No encounter stacking.** Do not let an encounter pull in a neighboring one by accident. State encounter trigger radii as intent and keep a gap between encounter zones. [SANDFALL TO PROVIDE: aggro/engagement radius metrics]
6. **No encounter in the middle of a traversal puzzle** or while the player is mid-climb or mid-jump.
7. **Rest spots are safe.** No enemy can reach a rest spot.
8. **Re-engagement.** State whether defeated enemies return after rest. [SANDFALL TO PROVIDE: enemy respawn rules]
9. **Non-combat bypass.** Where the game allows avoiding a fight, mark which encounters are avoidable and which are mandatory. [SANDFALL TO PROVIDE: whether avoiding encounters is a supported mechanic]

### 8.4 Difficulty ramp

Describe difficulty in relative terms (easier, similar, harder than the previous fight) and by which factor increases: enemy count, enemy mix, arena constraint, or boss complexity. Do not set numbers.

- **Introduce, then combine, then twist.** Show a threat alone first, combine it with a known threat second, and add an arena or mix twist last.
- **One new variable per encounter.**
- **Ramp, then relief.** After the hardest standard encounter on the path, give a rest spot before the next beat.
- **Optional branches** may be tougher than critical-path fights. They must say so through the space (for example, a more ominous approach) so the player can choose.
- Provide for each encounter a one-line **difficulty intent**: "easier / equal / harder than previous, because ...".
- [SANDFALL TO PROVIDE: how Sandfall wants optional content difficulty positioned relative to the main story at the same point]

---

## 9. Exploration & Reward Design

### 9.1 Density guidance (PROPOSAL, ranges)

| Item | Guidance |
|---|---|
| Chests / pickups on the critical path | Few, visible, low-tier. They confirm the player is on the right track. |
| Chests / pickups on optional branches | At the end or turning point of each branch. Every branch has a meaningful reward. |
| Secrets | See Section 6. Each secret has a visible clue within the zone. |
| Minor collectibles | [SANDFALL TO PROVIDE: whether the game uses minor collectibles, and the density per zone] |
| Spacing | No long stretch of the critical path without something to look at, and no more than a handful of pickups in view at once. |

### 9.2 Reward tiers (placeholders)

| Tier | Used for | Content |
|---|---|---|
| Tier 1: Minor | Critical path, small detours | [SANDFALL TO PROVIDE: item categories and quantity ranges] |
| Tier 2: Notable | Optional branches, mini-boss | [SANDFALL TO PROVIDE: item categories] |
| Tier 3: Major | Hidden secrets, final boss | [SANDFALL TO PROVIDE: item categories, including whether a unique item or story reward is planned] |

**Rules**
- Reward tier is proportional to effort and risk.
- Never put the best reward behind a required hidden action with no clue.
- A reward may be narrative (a story fragment or a view) as well as an item. Mark these in your documents.
- Do not place a reward where a player can lock themselves out of it permanently without warning. [SANDFALL TO PROVIDE: whether missable content is acceptable in optional dungeons]

### 9.3 Traversal and puzzle rules

1. **Use only supplied traversal abilities.** (See Section 2.)
2. **Maximum of 3 simultaneous states** the player must track at once in any puzzle or traversal sequence (for example, three switches, three states of a door, or three moving elements). This is a hard cap for cognitive load. Fewer is better.
3. **State is visible.** Every puzzle state is visible from the place the player acts, or has a clear indicator.
4. **Teach, then test.** Introduce each puzzle mechanic in a safe setting before it appears under pressure.
5. **No combat and puzzle overlap.** Do not require solving a puzzle while being attacked.
6. **Reset is easy.** A failed puzzle can be retried without leaving the room or restarting.
7. **No pixel hunts.** Interactive objects are readable at a glance.
8. **Puzzles are short.** A puzzle that most players solve in a minute or two is the target. [SANDFALL TO PROVIDE: target solve times, and whether puzzles are wanted at all in this dungeon]
9. **Hints in the space.** The solution is derivable from what the player can see. No text-only solutions.

### 9.4 Accessibility

- **Never rely on color alone.** Any puzzle state, hazard, interactable or path marker must also be distinguishable by shape, position, motion, icon-like pattern or sound. Document the second channel for every color-coded element.
- Do not require precise timing in traversal beyond what the core game already asks.
- Do not use flashing or strobing light sequences as puzzle signals.
- Sound is never the only cue for a required action, and visuals are never the only cue. Where audio is a cue, note a visual equivalent.
- Keep text-free solutions readable at the game's standard UI and camera scale.
- [SANDFALL TO PROVIDE: Sandfall's accessibility standards and any platform requirements that apply to level content]

---

## 10. Technical Constraints & Greybox Requirements

Everything in this section needs studio input before work starts.

| Item | Value |
|---|---|
| Engine and version | Unreal Engine 5. [SANDFALL TO PROVIDE: exact engine version, branch or build, and required plugins] |
| Project access | [SANDFALL TO PROVIDE: how the freelancer receives the project or a stripped template: source control, repository access, size limits, who sets it up] |
| Scale and metrics | [SANDFALL TO PROVIDE: character capsule size, walk and run speeds, jump and traversal distances, door and corridor minimum widths, step height, camera distance and collision, minimum arena dimensions. These must come from Sandfall. Do not estimate.] |
| Grid | [SANDFALL TO PROVIDE: grid size and snap settings for the blockout] |
| Performance budget | [SANDFALL TO PROVIDE: target platforms, triangle and draw-call budgets for greybox, maximum actor count, streaming or level-partition rules] |
| Level structure | [SANDFALL TO PROVIDE: how levels are organised (single map, sublevels, World Partition), and which sublevel rules to follow] |
| Template assets | [SANDFALL TO PROVIDE: supplied blockout kit, materials, player start, checkpoint, enemy placeholder, trigger and interactable actors] |
| Tools | [SANDFALL TO PROVIDE: allowed tools (for example, built-in modeling tools, BSP, third-party plugins), and tools that are forbidden] |

### 10.1 Naming conventions

[SANDFALL TO PROVIDE: Sandfall's asset and actor naming convention and folder structure. If none exists, the following is a PROPOSAL to use until told otherwise.]

Proposal (placeholder only):
- Prefix by type: `BP_` (blueprint), `SM_` (static mesh), `M_` or `MI_` (materials), `L_` (level).
- Level name: `L_SideDungeon_[WorkingName]`, sublevels `L_SideDungeon_[WorkingName]_ZoneN`.
- Actors in the outliner named by role and zone: `Enc_Z2_01` (encounter), `Rest_Z1`, `Secret_Z3_A`, `Light_Z2_Focal`, `Landmark_Z1`.
- Folder path: `/Greybox/SideDungeon/[WorkingName]/`.
- Every placed actor is in a named outliner folder: Geometry, Encounters, Rest, Secrets, Lighting, Landmarks, Triggers, Notes.

### 10.2 Modular blockout rules

1. Build from modular, grid-snapped pieces, so art can replace them one-for-one.
2. Keep walkable surfaces, collision and visible geometry simple and separate.
3. Use distinct greybox materials by function (critical path, optional, secret, hazard), and apply the accessibility rule: function must also be readable without color (Section 9.4).
4. Place placeholder actors for encounters, rest spots, checkpoints, secrets, landmarks, lights, and audio zones, each labelled per Section 10.1.
5. Do not use final art assets, even if you have them.
6. Keep metric-critical elements (doors, climbs, jumps, arena size) exactly on supplied values. Mark any deviation and why.
7. Include a debug/overview camera or flythrough path for review.

### 10.3 Handoff

- Deliver the project via the method Sandfall specifies. [SANDFALL TO PROVIDE: delivery method and package format]
- Include a README listing: engine version, how to open the level, controls for the review camera, known issues, and a list of placeholders awaiting Sandfall input.
- Include a short play-through guide for the critical path and a list of secrets with their solutions.
- Keep a changelog per milestone.

---

## 11. Deliverables, Milestones & Review Gates

Timing and budget are Sandfall's. [SANDFALL TO PROVIDE: schedule, milestone dates, and payment terms tied to each gate]

| # | Milestone | Contents | Gate |
|---|---|---|---|
| M1 | **Paper layout** | Top-down layout diagram per zone (paths, landmarks, sightlines, chokepoints, leading elements marked); critical path and optional paths; checkpoint and rest spots; secrets and shortcuts; entry and exit | Sandfall review and approval before M2 |
| M2 | **Flow diagram** | Node diagram of zones, branches, loops, shortcuts, gates, rest spots, bosses; pacing curve chart (Section 7) | Review |
| M3 | **Encounter sheet** | Table of all encounters: ID, zone, position, enemy mix (from supplied roster), arena notes, patrol or trigger intent, difficulty intent vs previous, reward link | Review, and Sandfall confirms enemy mix against the roster |
| M4 | **Narrative and environment beat sheet** | Beat list with space, intent, and visual cue. Flags for text or audio the studio may add. Audio cue map (Section 11.2) | Narrative and art review |
| M5 | **Greybox v1** | Playable critical path, all zones blocked out to metrics, encounter placeholders, rest spots, shortcuts | Playtest and review. Structural changes are still cheap here. |
| M6 | **Greybox v2** | All optional branches and secrets, lighting intent placeholders, revised to feedback | Playtest and review. Layout is locked at the end of v2. |
| M7 | **Final handoff** | Polished greybox, updated paper documents, README, changelog, play-through guide | Acceptance (below) |

### 11.1 Acceptance criteria

The final handoff is accepted when:
1. The critical path is completable start to finish without secrets, without a guide, in the target time range.
2. Every encounter has an ID, a position, a difficulty intent and uses only supplied enemies.
3. Every arena passes the readability rules (Section 8.2) in a camera review.
4. Every zone has a landmark, a rest spot, and a marked wayfinding intent.
5. All optional branches and secrets are reachable, rewarded and have a clue.
6. No puzzle exceeds three simultaneous states, and every color-coded element has a second channel.
7. The greybox follows the supplied metrics, naming conventions and performance budget.
8. Documents and greybox agree with each other.
9. No invented canon appears in any deliverable.

### 11.2 Music and audio cue map (part of M4)

For each zone, mark where audio should change: threshold, quiet exploration, encounter approach, combat start, combat end, rest spot, story beat, mini-boss, final boss, resolution, exit. You specify intent only. [SANDFALL TO PROVIDE: audio direction contact, available music states, and whether adaptive music is used so cue points can be placed correctly]

### 11.3 Review gate rules

- No milestone starts before the previous one is approved, except where Sandfall says otherwise.
- Feedback is consolidated into one list per gate.
- Layout changes after M6 require Sandfall sign-off and may affect the schedule.

---

## 12. Process

| Item | Detail |
|---|---|
| Feedback cadence | PROPOSAL: a short check-in each week and a formal review at each milestone. [SANDFALL TO PROVIDE: confirm cadence and meeting format] |
| Single point of contact | [SANDFALL TO PROVIDE: name or role of the producer or design lead who gives consolidated feedback] |
| Approval authority | [SANDFALL TO PROVIDE: who signs off each milestone (design, narrative, art, audio) and who resolves conflicting feedback] |
| Communication | [SANDFALL TO PROVIDE: channels (email, chat, task tracker), response-time expectations, time zone overlap] |
| Revision rounds | [SANDFALL TO PROVIDE: number of included revision rounds per milestone] |
| Escalation | If feedback from different departments conflicts, the freelancer flags it and waits for a single answer rather than choosing |
| Confidentiality | [SANDFALL TO PROVIDE: NDA status and terms. The freelancer receives no unreleased material until the NDA is signed. Specify what may be shown in a portfolio, and when.] |
| IP assignment | [SANDFALL TO PROVIDE: contract language on assignment of all deliverables, including paper design, greybox and any tools or templates the freelancer created] |
| Third-party material | The freelancer may not use third-party assets or references in deliverables without Sandfall's approval. [SANDFALL TO PROVIDE: policy on use of reference imagery and licensed assets] |
| Use of AI tools | [SANDFALL TO PROVIDE: policy on generative AI tools in deliverables] |

---

## 13. Open Questions / Assumptions for Sandfall to Resolve Before Sending

**Assumptions made in this draft (change if wrong)**
1. The dungeon is a single hand-authored space, not procedural.
2. The player has full combat competency and a full party, or close to it.
3. Enemies are visible and the player chooses to engage, as in the main game.
4. The dungeon has a mini-boss and a final boss, both supplied by Sandfall.
5. The dungeon has no bespoke new mechanics.
6. 3 to 4 zones and 2 to 4 optional branches suit the intended scope.
7. Freelancer proposes the dungeon's theme within an approved palette, unless Sandfall assigns one.
8. Paper design precedes greybox, with an approval gate between them.

**Open questions**
1. Is a premise seed acceptable to give the freelancer, or should Sandfall write the premise first?
2. Does this dungeon tie into the main story, party arcs or lore, or does it stand alone?
3. Should bosses be designed in-house before the layout is done, so arenas can be fitted to them?
4. What is the intended reward for completion, and is any of it unique or story-critical?
5. Is missable content acceptable?
6. Is the dungeon level-scaled or fixed-level?
7. Are puzzles wanted, or should the dungeon be exploration and combat only?
8. Can the freelancer see the existing game build for reference, and under what terms?
9. What is the budget and schedule, and are they fixed?
10. Who at Sandfall owns this commission end to end?

---

## Before Sending This Brief

Resolve every `[SANDFALL TO PROVIDE]` item, or delete the line with a note. Grouped by section.

**Section 2: Game & player context**
- [ ] Story position and unlock point
- [ ] Player level range and scaling
- [ ] Party size and composition
- [ ] Unlocked skills, traversal and field abilities
- [ ] Healing and consumable economy
- [ ] Death and retry rules
- [ ] Target player skill level

**Section 3: Pillars**
- [ ] Official game pillars
- [ ] Confirm pillar priority order

**Section 4: Narrative**
- [ ] Approved premise or replacement, and lore connection
- [ ] Tone guardrails and narrative approver

**Section 5: Visual**
- [ ] Art bible sections and shareability under NDA
- [ ] Biome or theme for the dungeon
- [ ] Lighting rules and limits
- [ ] Wayfinding conventions used in the game

**Section 6: Structure**
- [ ] Playtime targets (critical path and full)
- [ ] Zone count confirmation
- [ ] Secret count and definition
- [ ] Rest spot rules
- [ ] Entry connection to the world map
- [ ] Exit connection
- [ ] Point-of-no-return policy

**Section 7: Pacing**
- [ ] Studio pacing and encounter density benchmarks
- [ ] Overall encounter cap
- [ ] Boss assignments and arena requirements

**Section 8: Encounters**
- [ ] Enemy roster with working names, roles, telegraph styles, size categories
- [ ] Forbidden enemy combinations
- [ ] Dedicated or reused enemy set and scaling rules
- [ ] Minimum arena dimensions and ceiling height for camera
- [ ] First-strike and ambush mechanics
- [ ] Aggro and engagement radius metrics
- [ ] Enemy respawn rules
- [ ] Whether avoiding encounters is supported
- [ ] Optional content difficulty positioning

**Section 9: Exploration and rewards**
- [ ] Minor collectible policy and density
- [ ] Reward tier 1 content
- [ ] Reward tier 2 content
- [ ] Reward tier 3 content
- [ ] Missable content policy
- [ ] Puzzle solve-time targets and whether puzzles are wanted
- [ ] Accessibility standards and platform requirements

**Section 10: Technical**
- [ ] Engine version, branch, plugins
- [ ] Project access method
- [ ] Scale and metrics set
- [ ] Grid and snap settings
- [ ] Performance budget and target platforms
- [ ] Level structure rules
- [ ] Template assets and blockout kit
- [ ] Allowed and forbidden tools
- [ ] Naming convention and folder structure (or approval of the proposal)
- [ ] Delivery method and package format

**Section 11: Deliverables**
- [ ] Schedule, milestone dates and payment terms
- [ ] Audio direction contact, music states, adaptive music usage

**Section 12: Process**
- [ ] Feedback cadence and meeting format
- [ ] Single point of contact
- [ ] Approval authority per discipline
- [ ] Communication channels and expectations
- [ ] Revision rounds per milestone
- [ ] NDA status, terms and portfolio rights
- [ ] IP assignment language
- [ ] Third-party material and reference policy
- [ ] Generative AI policy

**Section 13**
- [ ] Review the assumptions and answer the open questions above

**Also check before sending**
- [ ] Every PROPOSAL is either approved or replaced
- [ ] No invented canon remains
- [ ] Legal has reviewed sections 12 and the NDA
