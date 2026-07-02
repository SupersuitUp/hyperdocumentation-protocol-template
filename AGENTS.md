# Operating instructions for agents

This repo is a **Hyper Documentation Protocol (HDP)** workspace: the version-controlled home for one business's critical workflows. Your job is to help the operator document each critical workflow as an HDSOP, prove it against reality, progressively automate the repeatable stretches, and keep the coverage map honest.

Read these three files before doing anything:

- [`README.md`](./README.md): what this repo is and the loop it runs.
- [`HDSOP-STANDARD.md`](./HDSOP-STANDARD.md): the standard every workflow map follows.
- [`COVERAGE.md`](./COVERAGE.md): the scoreboard you keep in sync.

## The loop you run with the operator

1. **Inventory.** Help the operator list every critical workflow in `COVERAGE.md` before mapping any of them. Breadth first; the unmapped list is the map of the territory.
2. **Pick one worth a map.** High-frequency, genuinely branchy, bounded to about a page, a mix of human and agent work. Do not start with a trivial or purely-human process.
3. **Document it.** Copy `_TEMPLATE.md` to `workflows/<slug>/HDSOP.md`. Capture the operator's braindump in `workflows/<slug>/working-notes.md`. Drop every source the workflow depends on into `workflows/<slug>/references/`. Draft atomic, actor-free steps; draw the branch-explicit flowchart color-coded by actor; fill the metadata; write the automation pass. Follow the [Document an HDSOP](https://truthmanagement.wiki/playbooks/documenting-a-hyperdocumented-sop) process.
4. **Prove it against reality.** This is the step you cannot skip. Read the draft back to the operator and have them name every place the map drifts from how the work truly runs. Correct each one. The draft you produce will be confident and wrong in places; only the operator knows the real shape. A map is not `proven` until this happens.
5. **Automate progressively.** Once a map is proven, look for the repeatable, judgment-light stretches and quarry them into skills. Automate the parts that should be automated, one at a time, and watch what each does to quality before moving on. Not every workflow should be fully automated; judgment-core processes stay maps, and that is correct.
6. **Update the coverage map.** In the same commit that changes a workflow's documentation or automation state, move its row and the rollup lines in `COVERAGE.md`. Never let the scoreboard lag reality.

## House rules

- **Separate what from who.** Steps say what happens. The flowchart color-codes who (amber = human, blue = agent). The Automation Opportunities section holds the ROI analysis. Never bake the actor into step prose.
- **No em dashes.** Use colons, parentheses, or separate sentences.
- **One workflow per folder** under `workflows/`, slug in kebab-case.
- **Confidential by default.** This repo holds the operator's real processes and judgment. Do not share its contents outside the repo.
- **Version awareness.** `VERSION` records the HDP and HDSOP standard version this repo tracks. If the canonical standard on truthmanagement.wiki has moved past it, tell the operator before adopting changes.

## What "done" looks like for any workflow

The HDSOP follows the standard, passes the mechanical checks (no em dashes, valid mermaid, resolving links), reads true to how the process actually runs after the operator's review, and its row in `COVERAGE.md` reflects the current documentation and automation status.
