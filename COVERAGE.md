# Coverage map

*The work manager for this business. Two questions, tracked over time: how much of the business is documented, and how much of it is automated. This table is the scoreboard that keeps AI work focused on progressively automating real workflows instead of scattering across tools and half-built experiments.*

Keep this file current. Every time a workflow's documentation or automation status changes, move it here in the same commit. A coverage map that lags reality is worse than none, because it is trusted.

## Rollup

*Update these three lines whenever the table below changes.*

- **Critical workflows identified:** 1 (example only; replace with your real inventory)
- **Documented:** 0 proven / 0 mapped of 1 identified
- **Automation coverage:** 0 workflows at `automated`, 0 at `mostly-automated`; the rest are manual

Write one honest sentence about where the biggest untapped leverage is right now:

> _Example: the two workflows that eat the most owner attention (lead qualification and monthly reconciliation) are still fully manual and not yet mapped. Those are next._

## The inventory

One row per critical workflow. Add every workflow first, map them second. Seeing the whole territory unmapped is the point: it shows how much of the business currently lives only in someone's head.

| Workflow | Owner | Frequency | Business value | Doc status | Automation status | HDSOP |
|---|---|---|---|---|---|---|
| Qualify an inbound lead (EXAMPLE) | Sales lead | many-times-daily | high | `mapped` | `manual` | [link](./workflows/_example-qualify-inbound-lead/HDSOP.md) |

## Status ladders

**Documentation status** (how well the workflow is mapped):

| Status | Meaning |
|---|---|
| `unmapped` | Identified as critical, but no HDSOP yet. Lives in someone's head. |
| `drafting` | An HDSOP draft exists but has not been reviewed against reality. |
| `mapped` | The HDSOP is written to the standard: steps, flowchart, metadata, automation pass. |
| `proven` | Reviewed against reality by the operator; every drift corrected. This is the only status you trust for automation. |

**Automation status** (how much of the proven map runs without a human):

| Status | Meaning |
|---|---|
| `manual` | A person does every step. |
| `assisted` | AI helps ad hoc, but nothing repeatable is packaged. |
| `skill-partial` | Some repeatable stretches are crystallized into skills. |
| `mostly-automated` | Most steps run via skills; the human is left at the judgment nodes. |
| `automated` | Runs end to end; a human only touches the irreducibly-human decisions. |

## How to read this

- A row at `unmapped` is pure risk: the process depends entirely on a person and cannot be taught, audited, or automated.
- A row at `proven` + `manual` is your best next automation target: you understand it, so anything you build automates a process you actually know.
- A row at `automated` is attention bought back. That is the whole point of the protocol.

Progress is one row moving one notch, most weeks. That is what winning looks like here. It is boring on purpose.
