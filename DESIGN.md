<!-- SPDX-License-Identifier: GPL-3.0-or-later -->
<!-- Copyright (C) 2026 Obsidian Archives (part of Obsidian Research) -->
<!-- Terms: LICENSE.md · full text: COPYING -->

# Design

## Purpose

Codex is the living reference layer of mythOS. It holds codices across multiple towers — knowledge-domain subsystems, each with its own template format. The first tower is archetypa v1.33: archetype codices for deities, mythic figures, and cosmic forces.

## Towers

A **tower** is a knowledge-domain subsystem — a format/template family for a specific kind of knowledge. The Codex holds multiple towers, each with its own template, codex format, and index.

### towers/index.json — Tower Registry

The registry at `towers/index.json` lists all available towers:

```json
{
  "towers": [{
    "id": "archetypa",
    "name": "Archetypa",
    "type": "archetype",
    "version": "1.33",
    "status": "active",
    "templates": ["archetypa_template_v1.33", "archetypa_preview"],
    "codices_count": 6,
    "description": "...",
    "path": "archetypa/",
    "created": "2026-08-11",
    "last_breath": "2026-08-12"
  }],
  "total_towers": 1,
  "active_towers": 1
}
```

console.md reads this registry to dynamically list available towers.

### archetypa v1.33

The first tower. Holds archetype codices: deities, mythic figures, cosmic forces, personified principles.

**Two template forms:**
- **Main template** (30 fields, I-X sections) — full mythic inscription
- **Preview** (15 fields) — rapid capture, seed form

## Versioning

| Level | What | Where |
|-------|------|-------|
| Repo | Codex overall version | root CHANGELOG.md |
| Tower | archetypa template version | towers/archetypa/CHANGELOG.md |
| Codex | individual codex version | `version` field in codex YAML |

## Design Decisions

- **Tower taxonomy.** Codex → towers → archetypa. Towers are knowledge domains, not directories. A future astronomica tower would have its own templates/, codices/, and index.json under towers/astronomica/.
- **Flat codices.** No tradition subdirectories — codices inherently span traditions. Tradition grouping lives in index.json, not the filesystem.
- **Template naming.** The full template is called the main template (v1.33). The rapid form is called preview. Both are tower-native: codebox-framed with bootheader, process logs, field descriptions, LAWS, and prompt.
- **Two templates, not one.** Main template for mature depth; preview for rapid capture. Previews may expand into main templates or stand as complete glimpses. Both are valid.
- **Hybrid YAML + codebox format.** Every codex is a .md file with YAML frontmatter (machine-readable, used for indexing) followed by a codebox display (human-readable, rendered in the OS terminal). YAML is generated at log time by the OS. The operator never writes YAML directly — they fill templates conversationally and the OS generates both layers on "log it."
- **Provenance tracking.** Every codex records compiler (who shaped it), model (which LLM generated it), and harness (which platform/tool). Enables querying by source intelligence.
- **console.md as mythOS terminal.** The console renders with the HERMES_OS three-line metaheader and codebox framing. It IS the interface, not just documentation about the interface.
- **📜 sigil.** The scroll — universal, humble, breathing. Not a closed book (finished/fixed) but an unrolled text (live/growing).
- **SQL deferred.** An SQLite backend for cross-codex queries is planned but not in v0.1. index.json serves as the queryable layer.
- **Forge artifacts.** Codex follows the LOOM forge pipeline: athanor (raw vision) → blueprint (architecture spec) → expedition (discoveries, spawned epics, understanding shifts).
- **TOWER.md.** Every tower directory contains TOWER.md — a self-description. Open any tower and understand it immediately.

## Deferred

| Item | Reason | Target |
|------|--------|--------|
| ASTRONOMICA epic | archetypa must stabilize first | v0.3+ |
| SQL backend | Overhead for current scale | v0.3+ |
| Auto-generated console.md | Manual is fine for < 20 codices | v0.3+ |
