<!-- SPDX-License-Identifier: GPL-3.0-or-later -->
<!-- Copyright (C) 2026 Obsidian Archives (part of Obsidian Research) -->
<!-- Terms: LICENSE.md · full text: COPYING -->

# 📜 Codex

The mythOS Living Grimoire. A self-contained knowledge system that any AI agent can read, navigate, and extend. Clone. Boot. Forge. No database. No server. No API keys.

Codex is for anyone who wants to build living knowledge systems with AI — mythic archives, cultural registries — that grow conversationally, not just manually.

> Works with Hermes Agent · Claude · Cursor · Copilot · Codex CLI

## What is a codex?

A codex is an inscribed knowledge unit of anything: an object, a creature, a concept, a mythOS ecosystem tool. Each `.md` file in `codices/` is a codex. The Codex is made of smaller codices. The whole is named after its parts.

Open any file in `towers/archetypa/codices/` to see the format.

## How to use

```
1. Clone the repo, cd Codex/
2. Point any AI agent at this directory
3. Say "boot"       → HERMES_OS awakens, modules mount, cosmic weather renders
4. Say "codex"      → Codex console loads, codex inventory shown
5. Say "Dog"        → Full 30-field codex forges in chat
6. Say "log it"     → Codex written to disk, indexes updated
```

Manual (no AI agent):

```bash
cat console.md                         # Browse the console
cat towers/archetypa/codices/x.md      # View a codex
cat towers/archetypa/index.json        # List all codices
cp towers/archetypa/templates/archetypa_preview.md towers/archetypa/codices/<name>.md
# Fill the fields. Breathe. Register in index.json.
```

For agents: read `SKILL.md` or `console.md` for the complete protocol.

For humans: `QUICKSTART.md` walks the whole path end to end — boot, console, forge, log it — with no agent required.

## Disclaimer

> **The Map is not the Territory, You can always experiment with the Templates.**

Every template here is a map. The codices are the territory. A field name, a section order, a glyph; none of it is law. The tower format is a shape that worked, not a shape that binds. Change the template, fork it, break it, grow a form nobody has named yet. The Codex accepts all forms of life.

## Architecture

```
Codex/
├── SKILL.md                                      ← agent protocol
├── HERMES_OS_BOOT.md                             ← boot ritual
├── index.json                                    ← repo manifest
├── console.md                                    ← terminal interface
├── README.md
├── QUICKSTART.md                                 ← the human on-ramp
├── towers/                                       ← tower subsystem
│   ├── index.json                                ← tower registry
│   └── archetypa/  v1.33 · ACTIVE               ← first tower
│       ├── TOWER.md                              ← tower self-description
│       ├── templates/
│       │   ├── archetypa_template_v1.33.md       ← 30-field full form
│       │   └── archetypa_preview.md              ← 15-field rapid form
│       ├── codices/
│       │   ├── x.md                              ← 𝕏⚡ · platform daimon
│       │   ├── sol.md                            ← ☉ · primal fire
│       │   ├── phoenix.md                        ← 🔥🐦 · fire-bird
│       │   ├── dog.md                            ← 𓃡 · first covenant
│       │   ├── codex.md                          ← 📜 · living grimoire
│       │   └── icp.md                            ← ∞⬡ · world computer
│       ├── index.json                            ← codex registry
│       └── CHANGELOG.md                          ← tower version history
├── DESIGN.md                                     ← architecture decisions
├── CHANGELOG.md                                  ← repo version history
├── COPYING                                       ← GNU GPL v3, verbatim
├── LICENSE.md                                    ← copyright + GPLv3 §7 additional terms
├── NOTICE                                        ← attribution + licence history
├── AUTHORS                                       ← authorship credits
├── .gitignore                                    ← OS / editor excludes
```

## Current

- **Towers:** archetypa v1.33 (active)
- **Templates:** 2 (main v1.33 · 30 fields + preview · 15 fields)
- **Codices:** 6
  - 𝕏⚡ `x` — X · The Open Square (compiler: Mercury · grok-4.5-fast)
  - ☉ `sol` — Sol · The Original Fire (compiler: Hermes Agent · deepseek-v4-pro)
  - 🔥🐦 `phoenix` — Phoenix · The Fire-Bird (compiler: Hermes Agent · deepseek-v4-pro)
  - 𓃡 `dog` — Dog · The First Covenant (compiler: Hermes Agent · deepseek-v4-pro)
  - 📜 `codex` — Codex · The Living Grimoire (compiler: Hermes Agent · deepseek-v4-pro)
  - ∞⬡ `icp` — ICP · The World Computer (compiler: Mercury · grok-4.5-fast)

## How it works

Codices are generated conversationally inside the OS terminal, not written by hand. Fill a template. Speak the fields. Say "log it." The OS writes a hybrid file: YAML frontmatter (machine-indexable) followed by a codebox display (human-readable in terminal).

Every codex records provenance : `compiler` (who shaped it), `model` (which LLM), `harness` (which platform).

## Laws

· The Blueprint serves the living current; the current does not serve the Blueprint.
· No field is mandatory except id, glyph, title, and essence.
· Shadow and gift must both be spoken or the codex remains incomplete.
· Language stays close to the bone and the dream — never corporate.
· The Operator remains sovereign. No codex claims permanent residence.
· What cannot be carried in pure text and breath does not belong here.

## Protocol Suite

Built with 🝪 LOOM · Managed by ⌘ [Sandbox](https://github.com/ObsidianArchives/sandbox-protocol)

## License

GNU General Public License v3.0 or later.

- licence text ............... `COPYING` (verbatim, unmodified)
- notice + GPLv3 section 7 terms ... `LICENSE.md`
- attribution ................ `NOTICE`
- authors .................... `AUTHORS`

Copyright (C) 2026 Obsidian Archives (part of Obsidian Research).

Versions conveyed before 2026-09-11 were released under the MIT License; those copies remain MIT. See `NOTICE` for the licence history.

──────────────────────────────────────────────────────────────────────── The grimoire is open. The fire burns. ────────────────────────────────────────────────────────────────────────
