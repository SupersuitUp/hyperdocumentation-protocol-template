# Hyperdocumentation Protocol (HDP) workspace

A version-controlled home for your business's critical workflows. You map each one to the **HDSOP** standard (a Hyperdocumented SOP: dual-readable by a human and an agent), prove the map against reality, then progressively automate the repeatable stretches. [`COVERAGE.md`](./COVERAGE.md) tracks how much of the business is documented and how much is automated, so the work stays focused instead of scattered.

> ## ⚠️ Before You Fork
>
> This template is public. **Your fork should be private.** When you click "Use this template", set Repository Visibility to **Private** before creating the new repo. This repo will hold your business's real processes, judgment, and reference materials.
>
> *If you forget, change visibility later in Settings → Danger Zone → Change visibility. Anything pushed while public is in the commit history; rotate anything sensitive that was exposed.*

## What this is

Most AI work is scattered. People chase tools, build half-finished experiments, and cannot say at the end of the month what actually got better. The Hyperdocumentation Protocol replaces that with a boring, legible loop:

1. **List your critical workflows.** The processes the business actually runs on.
2. **Document each one as an HDSOP.** A branch-explicit, metadata-rich map a human can follow and an agent can execute. See [`HDSOP-STANDARD.md`](./HDSOP-STANDARD.md).
3. **Prove the map against reality.** The one step you cannot skip. The first draft is confidently wrong in places; you read it back against how the work truly runs and fix every drift.
4. **Progressively automate.** Quarry reusable agent skills out of proven maps, one repeatable stretch at a time.
5. **Track coverage.** Every workflow has a documentation status and an automation status in [`COVERAGE.md`](./COVERAGE.md). That table is your scoreboard.

You do not automate a process you have not mapped. You map it, prove it, then automate the parts that should be automated.

**Canonical method:** [Hyperdocumentation Protocol](https://truthmanagement.wiki/concepts/hyperdocumentation-protocol) and [Documenting a Hyperdocumented SOP](https://truthmanagement.wiki/playbooks/documenting-a-hyperdocumented-sop) on truthmanagement.wiki.

## Repo layout

```
your-business-workflows/
├── README.md                 # this file
├── VERSION                   # the HDP + HDSOP standard version this repo tracks
├── COVERAGE.md               # the work manager: every critical workflow × (documented?, automated?)
├── HDSOP-STANDARD.md         # what makes a map an HDSOP, and the separation-of-concerns rules
├── _TEMPLATE.md              # blank HDSOP to copy for each new workflow
├── AGENTS.md                 # operating instructions for any agent working in this repo
├── CLAUDE.md                 # points Claude Code at AGENTS.md
└── workflows/
    ├── README.md             # the folder convention
    └── <workflow-slug>/
        ├── HDSOP.md          # the readable map (the doctrine)
        ├── working-notes.md  # the running interview capture and ground truth
        └── references/       # every source the workflow depends on
```

An `_example-qualify-inbound-lead/` folder ships as an illustration. Delete it once you have your own.

## Quick start

1. **Fork this template private.** "Use this template" → "Create a new repository" → Visibility **Private**. Name it for your business (e.g. `acme-workflows`).
2. **Clone it and open it in your agentic harness** (Claude Code, Hermes, Codex).
3. **Fill `COVERAGE.md` first.** Brain-dump every critical workflow in the business. Do not map any of them yet. Just list them. That list is the map of the territory.
4. **Pick the first workflow worth a map** (high-frequency, branchy, mixed human and agent work) and document it. Ask your agent to run the [Document an HDSOP](https://truthmanagement.wiki/playbooks/documenting-a-hyperdocumented-sop) process against `_TEMPLATE.md`.
5. **Prove it, then update `COVERAGE.md`.** Move the workflow's status. Repeat next week.

## The one rule that makes this work

The map an agent drafts will read as confident and be wrong in places. The step you cannot skip is **review against reality**: you read the draft back against how the process truly runs and name every drift. Only you know the real shape. Everything else is assembly the agent can do.

## License

Use this template however you like. No attribution required.
