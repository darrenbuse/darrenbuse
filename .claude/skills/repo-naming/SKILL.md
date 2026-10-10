---
name: repo-naming
description: How Darren names repos, tools and families of repos — a metaphor tight enough to write the first sentence of the description, then the GitHub description, the Side Projects line and the gh command. WHEN asked to name a repo, project, tool, module or group of repos, or to write a GitHub description or profile README listing line.
---

# Repo naming

Darren names things in a consistent way. The job is to produce names that sit alongside the ones he already has, then hand him the bits he always asks for next: a description, a listing line, and the command.

## Step 1: Work out what it is

Get these from the conversation. Don't ask up front; draft from what's there and ask one question at most, after the first batch.

- What it does, in one line, and the problem it solves. The problem matters more than the feature list. Belt (tickets moving along) was renamed once it turned out the real need was remembering where he left off. If the purpose shifts mid-chat, re-run naming.
- Which family it joins, if any. See the existing names at the end of this file.
- Product or utility.

Product: something he'll refer to by name, with its own identity. An app, a platform, a module, a bot, a server, a CLI he'll use daily.
Utility: a wrapper, a config repo, a template, an image, a plugin for something else. The other thing is the identity; this repo just serves it.

## Step 2: Generate

### The one rule

The name is a metaphor for what the thing does, and the metaphor has to be tight enough to write the first sentence of the description. That's the test.

- Retriever → "Fetches your repos like a good dog."
- Kobold → "The helpful spirit in the cupboard."
- dev-tin → "Crack it open, get to work."
- Jig → "Guides the cut so every piece comes out the same."

If you can't write that sentence, the name is a nice word and nothing more. Drop it.

Beyond that, in his words: slightly quirky, makes you smile, can be a bit clever, short-ish. One word for products. Real English, says aloud cleanly, no clever misspellings.

### Product mode

These are vocabularies he has drawn from so far. They are ideas to start from, not a boundary; a name from outside them is fine if it passes the test.

- Workshop and craft: Jig, Bench, Redpen, Stencil
- Household spirits and folklore: Kobold, Familiar, Puck
- Animals doing a job: Retriever
- Wayfinding: Waypoint, Sextant, Cairn
- Plain everyday verbs and nouns: Rummage, Legwork, Glean, Headsoup

Give 5 to 8 names, grouped, each with its description-first-sentence next to it so the link to function is visible. Say which you'd pick and why.

If the first batch reads as a conventional naming list (Sigil, Codex, Loom, Manifest), it's boring and he'll say so. Go again without waiting, with more mischief: servants and spirits (Majordomo, Factotum), small magic (Cantrip), things that don't take themselves seriously (Ploy).

Then check the family. Say the siblings aloud with the new name in the list: "Nexus, Thea, Kobold, Elsewhere". If it sounds like a different person named it, it's wrong.

One collision search: the name plus the ecosystem ("Trellis github mind map"). Avoid names that are already a big project in the same space. No registry checks; these are personal repos.

### Utility mode

Lowercase, hyphenated, two or three words, prefixed with the thing it wraps or the tool it's for. A joke is still welcome if the name invites one.

- tmux-projects, claude-template, pg-18-partman-timescale (plain)
- dev-tin, commit-o-matic (plain with a grin)

Prefixes already in use: `darrenbuse-` for personal identity repos (cv, brand), `archive-` for retired ones.

### Family or category names

When he asks for a name for a group (an ecosystem, a README section, a folder of repos), the name is the container the members sit in. Bench holds Jig, Redpen and Waypoint. Offer 4 or 5 with a one-line metaphor each, then show the full heading and member list once, under the pick, so he can see it in place. Don't repeat the member list under every candidate.

## Step 3: Finish with the bits he'll ask for anyway

Once a name is picked, give all of these without being asked.

**GitHub description.** One line, two sentences at most. First extends the name's metaphor. Second says plainly what it does and how. "Tracks Claude token consumption" was rejected with "ok doesnt say how"; "from the source of truth" fixed it.

```
🐕 Fetches your repos like a good dog. Clone, sync, and rebase all your GitHub repos with one command.
🥫 Crack it open, get to work. An opinionated general-purpose devcontainer packed with the good stuff.
```

**README listing line**, matching his profile README:

```
- 👹 **Kobold** - IaC. The tiny server in the shoe cupboard that gives Nexus a home
```

Emoji, bold name, hyphen, one short line. Pick an emoji that fits the metaphor, not the category.

**The command**, ready to paste. Private by default. Public only when it's useful to someone else (Retriever, pg-18-partman-timescale).

```bash
gh repo create Retriever --public --description "🐕 Fetches your repos like a good dog. Clone, sync, and rebase all your GitHub repos with one command."
```

Products Title-Case (Kobold, Trellis). Utilities lowercase (dev-tin).

**Then ask one question:** does he want it added to the Side Projects list on his profile README (darrenbuse/darrenbuse)? Ask for private repos too; the list already has private ones on it. If yes and you have a way to edit the repo (gh CLI, a connected GitHub tool, a linked machine with a checkout), add the listing line to README.md in the same section and show the diff. If you can't edit it, give him the line and say where it goes. Ask this on its own, not bundled with other questions.

## What not to do

- Don't ask "which direction do you prefer" before showing names. Show names, then ask one question if needed.
- Don't suggest names that only work if you know the backstory.
- Don't pad with org prefixes, SEO length rules, or registry checks.
- Don't praise his choice. "Bench it is." is enough.

## Existing names

Use these to check a new name sits alongside its siblings. The metaphor or description is in brackets.

### Nexus family (personal platform and home)
- Nexus - personal omni-app platform (the point where everything converges)
- Substrate - event-driven runtime under Nexus (the layer things grow on)
- Thea - ambient home interface ("manage your home based on how you want to feel, not what you want to control")
- Kobold - the small server in the cupboard that hosts Nexus (German household spirit, works unseen)
- Battery-Vigil - battery alerts that keep reminding you

### Bench family (developer workflow tools)
- Bench - the workbench the tools live on
- Jig - template-driven development (guides the cut so every piece matches)
- Redpen - edit and comment on markdown, used for reviewing specs
- Waypoint - side project tracking; earlier candidates Belt and Cairn (a marker left on the trail)
- Claudery - personal AI collaboration preferences for Claude Code
- Stencil - design system

### Notes and knowledge
- Rummage - search across notes and comms (digging through drawers)
- Trellis - mind map over Obsidian markdown ("structure that supports branching growth")
- Headsoup - his data in Trellis format ("a massive interconnected mindmap of thoughts")
- Legwork - workplace note management and automations
- Glean - browsing history (gathering what's left behind)
- Sextant - navigation/orientation

### Machines and infra
- Dotto - dotfiles ("the dots that make my machines feel like home")
- Retriever - clones, syncs and rebases all your repos ("fetches your repos like a good dog")
- dev-tin - devcontainer ("crack it open, get to work")
- commit-o-matic - cron and git-hook auto commits
- tmux-projects - tmux plugin, sessions named area/project
- pg-18-partman-timescale - Postgres image
- claude-template - repo template

### Work and Claude tooling
- Claude-Toll - scrapes Claude's usage page (the toll for passage)
- Engineering-Leader-Codex - curated prompts and agents
- Artificer - agent that creates and reviews agents

### Prefixes
- darrenbuse- for personal identity repos (darrenbuse-cv, darrenbuse-brand)
- archive- for retired repos (archive-Nexus)

### Profile README format

```
## 🛠 Side Projects - no warranties, no regrets

- 🚀 **Nexus** - My personal omni-app platform
- 🏺 **Thea** - Elegant home dashboard that isn't just a set of industrial dials
- 👹 **Kobold** - IaC. The tiny server in the shoe cupboard that gives Nexus a home
- 🎯 **Dotto** - Dotfiles. The dots that make my machines feel like home
```

GitHub user: darrenbuse
