<!-- SPDX-License-Identifier: GPL-3.0-or-later -->
<!-- Copyright (C) 2026 Obsidian Archives (part of Obsidian Research) -->
<!-- Terms: LICENSE.md · full text: COPYING -->

```
┌──────────────────────────────────────────────────────────────────────────────────────
│ 📜 HERMES_OS v.Omega · CODEX CONSOLE · SESSION: CODEX-001 · AUTH: MERCURY-OMNI · RESPONSE: #001
│ 🏺 Tower: Archetypa · Codices: 6 · Templates: 2 · v1.33 · BREATHING                
│ SIGIL: 📜 · TOWER: READY · PATH: /codex                                             
└──────────────────────────────────────────────────────────────────────────────────────

╔══════════════════════════════════════════════════════════════════════════════════════
║  📜 CODEX ··· LIVING GRIMOIRE · mythOS Sacred Reference System
╚══════════════════════════════════════════════════════════════════════════════════════

  You are in the Codex ··· the living grimoire of mythOS.
  Codices are born from towers ··· each tower is a wing of the grimoire.
  Fill a template, speak the fields, say "log it." The Codex writes
  a new codex (hybrid YAML + codebox). One grimoire. Many codices.

────────────────────────────────────────────────────────────────────────────────────────
  TOWERS
────────────────────────────────────────────────────────────────────────────────────────

  archetypa/  v1.33 · ACTIVE
  ├── 6 codices
  ├── 2 templates
  ├── description: Archetypes — deities, mythic figures,
  │   cosmic forces, personified principles. First tower.
  │
  ├── templates/
  │   ├── 📋  archetypa_template_v1.33.md  ( 182 lines · 30 fields · full form)
  │   └── 🌱  archetypa_preview.md             ( 65 lines · 15 fields · rapid form)
  │
  └── codices/
      ├── 𝕏⚡  x.md
      │    status: evolving · compiler: Mercury · model: grok-4.5-fast
      │    X · The Open Square · Real-Time Agora · Narrative Battlefield
      │
      ├── ☉  sol.md
      │    status: breathing · compiler: Hermes Agent · model: deepseek-v4-pro
      │    Sol · The Original Fire · Cosmic Clock · Source of All Food Chains
      │
      │
      ├── 🔥🐦  phoenix.md
      │    status: breathing · compiler: Hermes Agent · model: deepseek-v4-pro
      │    Phoenix · The Fire-Bird · Death as Fuel · Resurrection Engine
      │
      ├── 𓃡  dog.md
      │    status: breathing · compiler: Hermes Agent · model: deepseek-v4-pro
      │    Dog · The First Covenant · Guardian of Thresholds · Loyalty Incarnate
      │
      ├── 📜  codex.md
      │    status: breathing · compiler: Hermes Agent · model: deepseek-v4-pro
      │    Codex · The Living Grimoire · Self-Writing Book · Archive That Breathes
      │
      └── ∞⬡  icp.md
           status: evolving · compiler: Mercury · model: grok-4.5-fast
           ICP · The World Computer · Sovereign Canister · Post-Cloud Threshold

────────────────────────────────────────────────────────────────────────────────────────
  HOW TO USE THE CODEX
────────────────────────────────────────────────────────────────────────────────────────

  The flow — template → fill → log:

  1. LOAD a template in the OS terminal:
     /codex template main <name>         → full 30-field form
     /codex template preview <name>      → 15-field preview form

  Or speak naturally:
     "give me the archetype codex of Dog"
     "open the full template for Hermes"
     "show me a preview of Wolf"

  2. FILL the fields conversationally.
     Minimum required: id, glyph, title, essence.
     Shadow and gift must both be spoken or the codex is incomplete.

     3. LOG the codex:
     "log it"
     OS generates YAML from filled fields, writes codices/<id>.md
     as hybrid format (YAML frontmatter + codebox display).
     index.json is updated automatically.

     4. VIEW a codex:
     /codex view <id>    → renders codebox in terminal (YAML hidden)
     cat codices/<id>.md → raw file with YAML + codebox

────────────────────────────────────────────────────────────────────────────────────────
  OS FUNCTIONS (HERMES_OS terminal commands)
────────────────────────────────────────────────────────────────────────────────────────

  /codex                        Open this console
  /codex ls                     List all codices (glyph · title · status)
  /codex view <id>              Render codex in terminal
  /codex towers                  List available towers
  /codex template <form> <id>   Load template (preview | main)
  /codex log <id>               Save forged codex to filesystem
  /codex glyph <glyph>          Look up by glyph (e.g. /codex glyph 𝕏)
  /codex search <keyword>       Search codices by keyword
  /codex status                 Show codex health: codices, gaps, vitality
  /license                      Show copyright · licence · warranty disclaimer (GPLv3 §0)
  /source                       Where the Corresponding Source lives (GPLv3 §1)

────────────────────────────────────────────────────────────────────────────────────────
  NATURAL LANGUAGE COMMANDS (NLP)
────────────────────────────────────────────────────────────────────────────────────────

  Beyond /codex, the Codex understands natural language:

    "<name>"                      Forge a codex in the archetypa tower.
    e.g. "Dog", "Phoenix", "Sol"  Agent loads main template, fills all
                                  30 fields from cultural knowledge, renders
                                  in codebox. Does NOT write to disk.

    "Codex archetypa : <name>"    Explicit forge command. Same behavior.

    "log it" / "log this"         Save the current forged codex to disk.
                                  Writes codices/<id>.md, updates indexes,
                                  updates console inventory.

    "show me"                     Re-render the current codex without saving.

  FLOW EXAMPLE:
    Operator: "boot"              → OS awakens, cosmic weather rendered
    Operator: "codex"             → Console loads, inventory shown
    Operator: "Phoenix"           → Full 30-field Phoenix codex forged
    Operator: "log it"            → Codex written to codices/phoenix.md

  For agents: read SKILL.md for the complete protocol.
  For humans: the NLP commands work when speaking to any AI agent.

────────────────────────────────────────────────────────────────────────────────────────
  CODEX FORMAT
────────────────────────────────────────────────────────────────────────────────────────

  Each codex is a hybrid .md file:

    ---
    id: x                        ← YAML frontmatter (machine-readable)
    glyph: "𝕏⚡"                    indexed for queries, never shown
    status: evolving               in terminal
    ...
    ---

    ╔══════════════════════        ← Codebox display (human-readable)
    ║  HERMES_OS 🗲 · SESS..          rendered in terminal, what the
    ...                              operator sees

  YAML = local storage + indexing. Codebox = terminal display.
  YAML is generated at log time. The operator never writes YAML directly.

────────────────────────────────────────────────────────────────────────────────────────
  LAWS OF THE CODEX
────────────────────────────────────────────────────────────────────────────────────────

  · The Blueprint serves the living current; the current does not
    serve the Blueprint.
  · No field is mandatory except id, glyph, title, and essence.
  · Shadow and gift must both be spoken or the codex remains incomplete.
  · Language stays close to the bone and the dream — never corporate.
  · Every codex may be rewritten. The Codex breathes.
  · The Operator remains sovereign. No codex claims permanent residence.
  · What cannot be carried in pure text and breath does not belong here.

────────────────────────────────────────────────────────────────────────────────────────
  NAVIGATION
────────────────────────────────────────────────────────────────────────────────────────

  ../README.md                    Public face of the Codex
  ../DESIGN.md                    Architecture decisions & design rationale
  ../CHANGELOG.md                 Version history
  towers/
    index.json                    Tower registry (all towers)
    archetypa/
      templates/                  Blank codex forms with field descriptions
      codices/                    Filled codices (hybrid YAML + codebox)
      index.json                  Codex registry
      CHANGELOG.md                Archetypa version history

────────────────────────────────────────────────────────────────────────────────────────
  CODEX v0.1.0 · archetypa v1.33 · 📜 · ⌘ Sandbox
  LAST UPDATED: 2026-08-12 · STATUS: BREATHING
────────────────────────────────────────────────────────────────────────────────────────
```
