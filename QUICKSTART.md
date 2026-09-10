<!-- SPDX-License-Identifier: GPL-3.0-or-later -->
<!-- Copyright (C) 2026 Obsidian Archives (part of Obsidian Research) -->
<!-- Terms: LICENSE.md · full text: COPYING -->

# 📜 Codex Quickstart

Codex is a folder of flat files that an AI agent can read, navigate and extend. It is not software you install, not an app you run, not a database you connect to. You point an agent at this directory, say "boot", and a terminal opens inside your chat. You forge an entry there and look at it. Nothing reaches your disk until you say "log it".

This is the human on-ramp — ten minutes, nothing installed. Agents should read `SKILL.md` instead.

────────────────────────────────────────────────────────────────────────────────────────
  1 · THE TEN-MINUTE PATH
────────────────────────────────────────────────────────────────────────────────────────

```
1. get the files ............... clone, download, or copy the folder
2. point your agent at it ...... any agent, any harness
3. say "boot" .................. the terminal opens, the tower loads
4. say "codex" ................. the console shows what is inside
5. say a name — any name ....... a codex is forged and rendered in your chat
6. say "log it" ................ the codex is written to disk
```

Steps 3 to 5 happen in the chat. Step 6 is the only step that touches your filesystem.

────────────────────────────────────────────────────────────────────────────────────────
  2 · BEFORE YOU START
────────────────────────────────────────────────────────────────────────────────────────

You need a folder, a terminal, and an AI agent if you want the conversational path. You do not need an install, a database, a server, an account, API keys, a build step or a package manager.

`HERMES_OS` is a terminal convention — a way of framing answers as codebox output — plus a persona for the agent. It is not an operating system, and nothing in this repo is compiled or executed. The files are markdown and JSON, plus a single .gitignore.

**With an agent** is the intended path: boot, forge in chat, log it. **Without an agent** the whole thing still works: read the files, copy a template, fill the fields, register the entry. It is simply slower.

────────────────────────────────────────────────────────────────────────────────────────
  3 · GET THE FILES
────────────────────────────────────────────────────────────────────────────────────────

```bash
git clone <url> Codex
cd Codex
```

No git? Download the folder and drop it anywhere. There is no install step and no dependency to resolve.

────────────────────────────────────────────────────────────────────────────────────────
  4 · BOOT THE OS
────────────────────────────────────────────────────────────────────────────────────────

Point your agent at this directory and say:

```
boot
```

What you should see: a boot line with modules mounted, the console opening, a short brief, and a navigation tree. If the agent only replies with ordinary prose, it has not booted — tell it: `read HERMES_OS_BOOT.md and SKILL.md, then boot`.

Boot is not magic and nothing is loaded into memory. The agent is reading three files: `HERMES_OS_BOOT.md` carries the ritual and the voice, `console.md` carries the format and the commands, and `SKILL.md` carries the protocol behind both. Delete them and the OS stops existing.

────────────────────────────────────────────────────────────────────────────────────────
  5 · THE TERMINAL IN YOUR CHAT
────────────────────────────────────────────────────────────────────────────────────────

`console.md` is not documentation about an interface. It is the response template. Every answer the agent gives you in Codex mode is that shape: a metaheader, a body, glyphs, rules, a footer.

The consequence matters: **a forged codex is displayed, not saved**. When you say "Dog", the agent loads the main template, fills thirty fields, and renders the whole thing in your chat. You are looking at a rendering. Close the tab and it is gone.

That is deliberate. The operator stays sovereign: nothing persists until you say so.

────────────────────────────────────────────────────────────────────────────────────────
  6 · OPEN THE CONSOLE AND LOOK AROUND
────────────────────────────────────────────────────────────────────────────────────────

Say `codex`. The console shows the tower, the entry count, the templates and every command it answers to.

| command | what it does |
|---|---|
| `/codex` | open the console |
| `/codex ls` | list codices — glyph · title · status |
| `/codex view <id>` | render one codex in the terminal |
| `/codex towers` | list the towers |
| `/codex template <form> <id>` | load a template — `preview` or `main` |
| `/codex log <id>` | write a forged codex to disk |
| `/codex glyph <glyph>` | look up an entry by glyph |
| `/codex search <keyword>` | search codices by keyword |
| `/codex status` | live health — counts, gaps, vitality |
| `/license` · `/source` | copyright, licence, and where the source lives |

With no agent at all, `cat` is enough:

```bash
cat console.md                        # the interface, in full
cat towers/archetypa/TOWER.md         # what this tower is
cat towers/archetypa/index.json       # the queryable map of every codex
cat towers/archetypa/codices/x.md     # one codex, frontmatter and all
ls  towers/archetypa/templates/       # the two forms
```

The map lives in `index.json`. The writing lives in `codices/`. Everything else is instructions.

────────────────────────────────────────────────────────────────────────────────────────
  7 · FORGE A CODEX
────────────────────────────────────────────────────────────────────────────────────────

Say one word — any name. `Dog`. `Phoenix`. `Wolf`. `Tuesday`.

The agent loads `towers/archetypa/templates/archetypa_template_v1.33.md`, fills thirty fields across sections I to X, and renders the codex in codebox. That is the main form. The rapid form, `archetypa_preview.md`, carries fifteen fields and exists for speed.

Two shapes live in one file:

    YAML frontmatter ...... machine-readable: id, glyph, title, status, provenance, relations
    codebox body .......... human-readable: the writing, the shadow, the gift, the approach

Four fields are the minimum for a valid entry: `id` · `glyph` · `title` · `essence`. Nothing else is mandatory. But a codex with no shadow and no gift is incomplete — both must be spoken or the entry stays unfinished.

Every codex also records provenance: `compiler` for who shaped it, `model` for which LLM, `harness` for which platform. That is how you can tell which mind made which entry, and argue with it.

Templates are maps, not law. Fork the shape, break it, grow a form nobody has named yet.

────────────────────────────────────────────────────────────────────────────────────────
  8 · FORGE WITHOUT AN AGENT
────────────────────────────────────────────────────────────────────────────────────────

```bash
cp towers/archetypa/templates/archetypa_preview.md towers/archetypa/codices/wolf.md
```

Open the new file. Fill the frontmatter and the body. Then register it in `towers/archetypa/index.json` so the tower, the console and any agent can find it.

A registry entry carries `id` · `glyph` · `title` · `status` · `traditions` · `keywords` · `file`. Copy an existing entry and edit it — the shape is already there.

────────────────────────────────────────────────────────────────────────────────────────
  9 · "LOG IT" — WHAT LANDS ON DISK
────────────────────────────────────────────────────────────────────────────────────────

Say `log it`. Three things happen, and only these three:

    codices/<id>.md ................... written — hybrid format, frontmatter plus codebox body
    towers/archetypa/index.json ....... the entry is registered
    console inventory ................. the count and the listing change

No database is created, no server starts, no account is made. Two files change and one view updates. That is the entire persistence model. If you took the manual path in section 8, you have already done it by hand.

────────────────────────────────────────────────────────────────────────────────────────
  10 · ADD A TOWER
────────────────────────────────────────────────────────────────────────────────────────

A tower is a knowledge domain with its own template family. One tower exists today, `archetypa`. A second domain gets its own directory and its own rules.

    towers/<name>/TOWER.md ............ what this tower is, in its own voice
    towers/<name>/templates/ .......... the forms an entry can take
    towers/<name>/codices/ ............ the entries themselves
    towers/<name>/index.json .......... the tower's own registry
    towers/<name>/CHANGELOG.md ........ how the tower's format evolved

Then register it in `towers/index.json`. Copy `towers/archetypa/` as your starting shape and rename what you keep.

────────────────────────────────────────────────────────────────────────────────────────
  11 · LAWS OF THE GRIMOIRE
────────────────────────────────────────────────────────────────────────────────────────

    The Blueprint serves the living current; the current does not serve the Blueprint.
    Four fields only are mandatory: id · glyph · title · essence.
    Shadow and gift must both be spoken, or the codex is incomplete.
    Language stays close to the bone and the dream — never corporate.
    The operator remains sovereign. No codex claims permanent residence.
    What cannot be carried in pure text and breath does not belong here.

No database. No server. No API keys. Flat files only.

────────────────────────────────────────────────────────────────────────────────────────
  12 · CHEAT SHEET
────────────────────────────────────────────────────────────────────────────────────────

| command | purpose |
|---|---|
| `boot` | wake the terminal |
| `codex` | open the console |
| `<name>` | forge an entry in chat, nothing written |
| `log it` | write the forged entry to disk |
| `/codex ls` · `/codex status` | inventory and live health |
| `/codex view <id>` · `/codex glyph <glyph>` · `/codex search <kw>` | find things |
| `/codex template <form> <id>` | load a form — `main` or `preview` |
| `/license` · `/source` | legal notices and upstream source |

| path | what it is |
|---|---|
| `SKILL.md` | the agent protocol |
| `HERMES_OS_BOOT.md` | the boot ritual and the voice |
| `console.md` | the terminal format and every command |
| `index.json` | the file map of the whole repo |
| `towers/index.json` | all towers |
| `towers/archetypa/TOWER.md` | the first tower |
| `towers/archetypa/index.json` | every codex in the tower |
| `towers/archetypa/templates/` | the two forms |
| `towers/archetypa/codices/` | the entries |
| `DESIGN.md` | why it is built this way |
| `COPYING` · `LICENSE.md` · `NOTICE` · `AUTHORS` | the legal layer |

────────────────────────────────────────────────────────────────────────────────────────
  13 · TROUBLESHOOTING
────────────────────────────────────────────────────────────────────────────────────────

**The agent replied but nothing booted.** It answered as an assistant instead of opening the terminal. Point it at the files: `read HERMES_OS_BOOT.md and SKILL.md, then boot`.

**The codex came out thin.** That is a prompt problem, not a format problem. Name a specific being or force, or forge the preview form first and expand it later.

**I logged it and lookups look wrong.** Check that entry in `towers/archetypa/index.json`. The fields that break lookups are `id`, `glyph`, `status` and `file` — and `file` must read `codices/<id>.md`.

**How do I find something?** Grep is the query engine:

```bash
grep -ril "threshold" towers/archetypa/codices/
grep -n '"id"'        towers/archetypa/index.json
```

**Where did the Cat codex go?** It was removed deliberately. It is retained in the project archives, not in this repository's history, and it will not return by accident.

**How many codices are there, really?** Ask the live surface, not a document: `/codex status`, or `ls towers/archetypa/codices/`. Counts written in prose go stale, which is why this guide avoids them.

**What this is not.** Not an app. Not a framework. Not a library. Not a database — grep is the query engine. Not scholarship — the myths here are written, not cited from sources. Not battle-tested — one author, one agent, no test suite and no CI. One tower exists. The deferred items live in `DESIGN.md`.

────────────────────────────────────────────────────────────────────────────────────────
  14 · LICENCE & ATTRIBUTION
────────────────────────────────────────────────────────────────────────────────────────

    licence ....... GNU GPL v3.0 or later
    text .......... COPYING — verbatim, unmodified
    terms ......... LICENSE.md, including the section 7 additional terms
    attribution ... NOTICE
    authors ....... AUTHORS
    copyright ..... Obsidian Archives (part of Obsidian Research)

The section 7 terms add four duties on top of the GPL: preserve the attribution, mark the origin of modified versions, do not use the project names for publicity, and no trademark rights are granted. If you fork or republish, carry `NOTICE` with it.

────────────────────────────────────────────────────────────────────────────────────────
  15 · WHERE TO GO NEXT
────────────────────────────────────────────────────────────────────────────────────────

    agents .......... SKILL.md — the complete protocol
    commands ........ console.md — the full terminal surface
    reasoning ....... DESIGN.md — why the format is the way it is
    the first tower . towers/archetypa/TOWER.md
    the whole map ... index.json

The grimoire is open. The fire burns.
